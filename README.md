# CommitTest
 test commit
..............

-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAkbS6elMP1as+NDGd1W+g6InpXRe/gCptnehDrsSxd2THEuiPIyH/sfNLNgN93juQag5itLzP5hOeWsDPv3yq
LHvEiyQUUyn+Sdg9SWKA6yTSNVPE2t6ftjpwhvBeeAhzQbApHoM07i+nd2x3XAjp
S5mfcxGoRQDA+zpAJ1oFogy/0FPtf0lASUfd0Acz1nA62ZrR+R2xhNGYdbzKXFSX
Y8OeEKK6eLp+T5hsQK/KuLuHURSv82FZAFN6GfauqEw6Ca424UZQ/llRE2kFgrix
LFkbm1HJaZu8pCmirDkQDX6khxiDby4UE1X018E4kISPyqfxSpxZt0JghxigSsxy
cQIDAQAB
-----END PUBLIC KEY-----
.............................

-----BEGIN ENCRYPTED PRIVATE KEY-----
MIIFNTBfBgkqhkiG9w0BBQ0wUjAxBgkqhkiG9w0BBQwwJAQQhWpXOGxSz6aDJ1Ou
2jJ7XwICCAAwDAYIKoZIhvcNAgkFADAdBglghkgBZQMEASoEEN5Grvo29Y657j9P
cadfJgwEggTQ44DPWSLJ2worzGQZ2WnfHdJPfr4hjdJonuTePaH6zF1ckBetMKY8
S/mSv7VgxqrNiSrvhxPPUk9E5zInvCWdwaV5pcaptrlWycBBkM+j0T9sO0k5TQpP
T2lPmQItn5/lya8uJ6Et6gzVZyoPURPCCi9dMbYxt0UGfefDfsUyQxZmXvY8s+Ad
3viDVWPUq23G6zK5JRunYfU2oRhWGkgjr1vEpGukCZYW2g9YqSP5Wlts6zXvVuLz
3NyY21oW8pURt/qVGnQvcn8EGq8iSv8pBkR9Ly0vG5qtJh5R6homRU354qOpzEDx
zTYLSEnigtGsfDbgsjV3/mzdpkgxq0O/Mpljrv8ntYKWm7kKp89tohEWIgCD+cPq
xhu3E2H4gtxOw8sNo9OXFl/tPGckfuE7Ih27dfD1XCUzSFhiSlQDUAiVG4byQNYt
lSKvic9jY+7eNMXwMytyApW50UBTAa7QnKaChwaqPnS3jyOXyNGmXH//BTKikdYf
aNDnJnq1HmbyBUqPrwqfzAdrE1E640Qb+OulLVM7I1EH4u5OpOh50Ea53V+vo28m
m3kwD32Hpsh5YI7FJm7Pu0iVwUXQtDjCDjvRANIXiSiAI0NuHFMVu+dAJ+6C6oTh
NSNN/PeocVHYW8vcRUGLCu/O3BlzPo//hcWMW0lo0Sh6IasXaTkbLG5MZSMga+j2
rv/PuvvvET8vlNXqup5WPsZX6ItvzmDBUfbcVHyzwP8dI+QE7hCOU2DXT7EAREw0
zjd34NZ238l9Kh1I6DxVfRwwxYjp4FExC6+bsKVHEsV9YCmPzJ4wVu4VeOODxtV6
ldXqBNI7/spvgCVGelzO2b/Sglny1hfYE7AUfKNXfgeMpl8uCBi8VOhkp5ac7De4
Lkj5RZpBrHCGjNXMBIgjWcFmSuWKYSbNMjXZgaCoUPXP3xlp6hp9z9lateTuTonH
Nyu8U2EBVDOouhmR8+ZrcYfuTvn2JpLx1V3K5Gz6FOiR5wpa0usX0ZHedmDXiDez
bS8OWSdTZfTlNkZV9iZckYGSUzqyOTihGg0htJyPZOjuQ76QttbAsE5L4c8S1uoQ
bGH1Y0bvhC2QdebjLn/kBCHOaL7EDvrwJ7PpVOr8M8RdGfeeK8UNLn5CrcyLG+lb
HIvB4DVL0w5zCUSQeVBn0xDBonxOJD4kJz3Q7YZFa3f/HKTU6CMIjf0AouEXGL30
w4BnmmyiT5IJs7+RAm2bU1nqyJDGGBg/TFqWPhOlkYXkVf+imvUXWMhn/3W8XWnz
JTrCNE3GoP0JM95lD5BgGH7K7u5oxve7uLAwyCg0D2UGGGUs1s4oX7kbeHrljugp
6pJwkVnvpatRTuesLcc+hYKvtPhGW8LZBqD9TzbA+238q3iyOpkrlKOg6an8jAFO
8Bhtt6/gitPtoHaDrX2Itj9yDHZgGEbTmOZXFucxHpBNLGbpgYzVM9LJtBp5QCAe
zqEBoXVwh4BqqScAKT2PiA7ZHmDiBhxCkyMMaxDg9lYmt0MZ+rcdl5ctMiAzX9mc
b+qCUZzDGbucGAg1yd1EKb0bLEVm4N1VZu5bKDtr16HlY0ixyqcX0IBe7Y90yq1d
T1cTm5TjcUC6uQJcntPgqi6sIu7bNH9w9o/MDtCeBNjb9fjgiy3Njlc=
-----END ENCRYPTED PRIVATE KEY-----

...........................................................
import java.security.*;

public class RSAKeyGenerator {

    public static void main(String[] args) throws NoSuchAlgorithmException {
        // Generate an RSA key pair with a key size of 2048 bits
        KeyPair keyPair = generateRSAKeyPair(2048);

        // Get the private and public keys
        PrivateKey privateKey = keyPair.getPrivate();
        PublicKey publicKey = keyPair.getPublic();

        // Print the keys (just for demonstration purposes)
        System.out.println("Private Key: " + privateKey);
        System.out.println("Public Key: " + publicKey);
    }

    public static KeyPair generateRSAKeyPair(int keySize) throws NoSuchAlgorithmException {
        // Initialize the key pair generator
        KeyPairGenerator keyPairGenerator = KeyPairGenerator.getInstance("RSA");

        // Initialize the key size
        keyPairGenerator.initialize(keySize);

        // Generate the key pair
        return keyPairGenerator.generateKeyPair();
    }
}
................



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

