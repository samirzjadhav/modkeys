# Mod access keys (hashed)

This file `keys.txt` is the allow-list for the mod menu.
Each line is the **SHA-256 hash** of an access key (not the key itself),
so the list can be public without exposing usable keys.

- One hash per line.
- To give access: add the hash of that person's key, and send them the plain key.
- To revoke: delete that line.

Make a hash for a new key (PowerShell):

    $s="JOHN-2201"; -join ([System.Security.Cryptography.SHA256]::Create().ComputeHash([Text.Encoding]::UTF8.GetBytes($s)) | %{$_.ToString('x2')})

Current test key: SAMIR-TEST-01

Raw URL the mod reads:
https://raw.githubusercontent.com/samirzjadhav/modkeys/main/keys.txt
