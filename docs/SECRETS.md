# Secrets

```bash
# Encoding to base64
echo "test" | base64
openssl rand -base64 32

# Applying encryption with SOPS. Make sure to have age.agekey
mise run encrypt-secret ./path/to/secrets.yaml
```
