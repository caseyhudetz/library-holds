# Library Holds for Alexa

Ask Alexa which of your library holds are ready for pickup.

> "Alexa, ask Chicago Library if my books are ready."
> "Pat, you have 2 books available: Piranesi and The Overstory. 1 more is in transit."

This repo hosts the account-linking page and privacy policy for the Library Holds Alexa skill. It works with Chicago Public Library cards.

## How sign-in works

- `index.html` is the page the Alexa app opens when someone links their library card.
- The card number, PIN and optional first name are encrypted **in the browser** with the skill's RSA public key (RSA-OAEP, SHA-256).
- The encrypted result is handed back to Alexa as the account-link token. Amazon stores it; nothing is stored on this site or any server.
- Only the skill holds the private key, so only the skill can decrypt it, and only when the person asks about their holds.
- Unlinking or disabling the skill in the Alexa app deletes the token.

## Privacy

See [privacy.html](privacy.html).

Library Holds is an independent project. It is not affiliated with or endorsed by Chicago Public Library, BiblioCommons or Amazon.
