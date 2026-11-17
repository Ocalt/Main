# 0002 - Storage that must be migrated to be unified

## Counter-design

**Ocaltio**. Source: https://ocalt.com and https://ocalt.com/docs/ocaltio.

- It unifies existing storage into one file explorer, with no migration. The backends are SFTP/SSH, FTP/FTPS, S3-compatible, WebDAV and machines running the OcaltQL Client.
- Vast Drives are named, encrypted pools of chosen backends, with unlimited pools, editable membership and combined capacity shown before confirming.
- Each file is stored whole on one backend, preferring the most free space.
- Ocalt keeps the index.
- Credentials are stored encrypted and never redisplayed.
- The user keeps the backends. Compromised endpoints are not covered.
