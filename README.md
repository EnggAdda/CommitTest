# CommitTest
 test commit


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

