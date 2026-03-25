# musical-parakeetimport base64

def try_decode(s):
    try:
        return base64.b64decode(s).decode('utf-8')
    except:
        return None

input_str = "o1hn8h6a7t1l7z7zq3om2t1e7i7f8v6gx5wg1t6s3u8z6l9fr1vj9c8n6u8i7p7dn4hs2e2w8k3m1l4hu3ys9b5t1y1z4q8jm5lk7l9u8z2s2g7b"

# Try filtering digits
filtered_chars = "".join([c for c in input_str if not c.isdigit()])
print(f"Chars only: {filtered_chars}")

# Try filtering letters
filtered_digits = "".join([c for c in input_str if c.isdigit()])
print(f"Digits only: {filtered_digits}")

# Check length
print(f"Length: {len(input_str)}")
