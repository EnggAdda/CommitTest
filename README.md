# CommitTest
 test commit

 <dependency>
    <groupId>com.nimbusds</groupId>
    <artifactId>nimbus-jose-jwt</artifactId>
    <version>9.10</version> <!-- or the latest version available -->
</dependency>


 import org.springframework.stereotype.Service;
import javax.crypto.Cipher;
import javax.crypto.spec.SecretKeySpec;
import java.security.Key;
import java.util.Base64;

@Service
public class EncryptionService {

    private static final String AES = "AES";
    private static final String SECRET_KEY = "yourSecretKey"; // Replace with your secret key

    public String encrypt(String data) throws Exception {
        Key key = generateKey();
        Cipher cipher = Cipher.getInstance(AES);
        cipher.init(Cipher.ENCRYPT_MODE, key);
        byte[] encryptedValue = cipher.doFinal(data.getBytes());
        return Base64.getEncoder().encodeToString(encryptedValue);
    }

    public String decrypt(String encryptedData) throws Exception {
        Key key = generateKey();
        Cipher cipher = Cipher.getInstance(AES);
        cipher.init(Cipher.DECRYPT_MODE, key);
        byte[] decryptedValue = cipher.doFinal(Base64.getDecoder().decode(encryptedData));
        return new String(decryptedValue);
    }

    private Key generateKey() {
        return new SecretKeySpec(SECRET_KEY.getBytes(), AES);
    }
}



...........................................................................



import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.*;

@RestController
@RequestMapping("/api")
public class YourController {

    @Autowired
    private EncryptionService encryptionService;

    @PostMapping("/encrypt")
    public String encryptData(@RequestBody String data) throws Exception {
        return encryptionService.encrypt(data);
    }

    @PostMapping("/decrypt")
    public String decryptData(@RequestBody String encryptedData) throws Exception {
        return encryptionService.decrypt(encryptedData);
    }
}
........................................................................................





// Assume you have already loaded private key from a file or generated it programmatically

import com.nimbusds.jose.*;
import com.nimbusds.jose.crypto.RSAEncrypter;
import com.nimbusds.jose.util.Base64;

@RestController
public class EncryptionController {

    @PostMapping("/encrypt")
    public ResponseEntity<String> encryptData(@RequestBody String data) throws Exception {
        // Load or generate private key
        PrivateKey privateKey = loadPrivateKey();

        // Create JWE header
        JWEHeader header = new JWEHeader.Builder(JWEAlgorithm.RSA_OAEP_256, EncryptionMethod.A128GCM)
            .contentType("text/plain")
            .build();

        // Create JWE object with payload
        JWEObject jweObject = new JWEObject(header, new Payload(data));

        // Create encrypter with the public key
        RSAEncrypter encrypter = new RSAEncrypter(privateKey);

        // Encrypt the payload
        jweObject.encrypt(encrypter);

        // Serialize to compact form
        String encryptedData = jweObject.serialize();

        return ResponseEntity.ok(encryptedData);
    }

    private PrivateKey loadPrivateKey() {
        // Load private key from a file or generate it programmatically
        // Return the private key
    }
}
................................................................

import { JWE, JWK } from 'jose';

async function decryptData(encryptedData) {
    // Fetch public key from server or use a stored public key
    const publicKeyResponse = await fetch('/publicKey');
    const publicKey = await publicKeyResponse.json();

    // Parse JWK (JSON Web Key) from public key
    const jwk = JWK.asKey(publicKey);

    // Parse JWE (JSON Web Encryption) from encrypted data
    const jwe = JWE.decrypt(encryptedData, jwk);

    // Access decrypted payload
    const decryptedData = jwe.payload.toString();

    return decryptedData;
}
////44


/////

