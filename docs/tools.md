# Tools

PieterPost MCP exposes tools for postal workflows, account context, payment links, and Mailbook contacts.

## Documentation Tools

- `search`: Search PieterPost API and MCP docs.
- `fetch`: Fetch a specific PieterPost document or account context item.

## Mail Tools

- `quote_order`: Price a letter or postcard before sending.
- `create_compose_link`: Create a PieterPost review link with prepared recipient and message data.
- `create_payment_link`: Create a hosted payment link for a prepared letter or postcard.
- `create_checkout_link`: Compatibility checkout link tool.
- `get_order`: Check order status.
- `upload_asset`: Upload supported assets, such as postcard front images, letter attachments, or letter stamp images.

## Mailbook Tools

- `list_mailbook_contacts`: Search saved contacts.
- `get_mailbook_contact`: Fetch one saved contact.
- `create_mailbook_contact`: Create a contact when authorized.
- `update_mailbook_contact`: Update a contact when authorized.
- `delete_mailbook_contact`: Delete a contact when authorized.

## Developer Tools

- `get_wallet`: Check API credit wallet balance.
- `create_credit_topup`: Create a wallet top-up checkout.
- `list_topups`: List top-ups.
- `get_topup`: Check a top-up.
- `create_direct_order`: Send directly with API credits. Use only for trusted workflows and explicit live-send confirmation.
- `list_api_keys`: List API keys.
- `create_api_key`: Create an API key.
- `revoke_api_key`: Revoke an API key.

## Payload Notes

Address input should be structured. Provide a recipient name plus `addressLines`, or structured fields such as `streetAddress`, `postalCode`, `city`, `state`, and `country`.

Custom postcard front images must be square, with a 1:1 aspect ratio.
