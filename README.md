# security.bobine.fit

Static vulnerability disclosure site for [Bobine](https://github.com/FantasmaGlad/Bobine), served by GitHub Pages at <https://security.bobine.fit>.

It publishes the OpenPGP key used to receive vulnerability reports, its fingerprint, a copy of the signed `security.txt` and a pointer to the full policy. It is a fingerprint verification channel that is independent of the main website `bobine.fit`.

French version: [README.fr.md](README.fr.md).

| File | Purpose |
|---|---|
| `index.html`, `fr/index.html` | home page in English (default) and French |
| `snake/index.html` | Snake game |
| `security.asc` | OpenPGP public key (fingerprint `23CA D324 C507 FB0F 97E6 AECA 6E4C 020E F8BD FEB2`) |
| `.well-known/security.txt` | copy of the signed file ([RFC 9116](https://www.rfc-editor.org/rfc/rfc9116)), identical to the one on `bobine.fit` |
| `CNAME`, `.nojekyll` | custom domain; `.nojekyll` is required for `.well-known` to be served |
| `robots.txt`, `sitemap.xml`, `llms.txt` | indexing |

## Maintenance

The key, its fingerprint and `security.txt` must stay identical to those on `bobine.fit` and in the Bobine repository (`docs/security/`). When the key is renewed or rotated, update this repository in the same operation and check that the fingerprint is the same on every channel.

A daily check verifies that the domain still resolves to this repository and that the fingerprint served is the expected one.

## License

AGPL-3.0, see [LICENSE](LICENSE).
