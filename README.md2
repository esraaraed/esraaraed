from Crypto.Cipher import AES
from Crypto.Util import Counter
import binascii


ct = "0af19d85a06c798dc2acf03a9da136e6862a7f04baa0d059ce52253fa8ac12ae"
key = "VERYSECRETKEY123"
iv = 46591467637275752715089622446234987666
ct_bytes = binascii.unhexlify(ct)
cipher = AES.new(key.encode(), AES.MODE_CTR, counter=Counter.new(128, initial_value=iv))
decrypted_data = cipher.decrypt(ct_bytes)
if decrypted_data.startswith(b"BAU"):
    print("Flag found:", decrypted_data.decode())
else:
    print("Flag not found in decrypted data.")

#BAU{Brut3_F0rcing_Is_Back_Again}
