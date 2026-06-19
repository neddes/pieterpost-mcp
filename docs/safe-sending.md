# Safe Sending Flow

PieterPost MCP can send real physical mail, so the recommended flow keeps the user in control.

## Recommended Flow

1. Resolve the recipient from user-provided structured address data or Mailbook.
2. Draft the final letter or postcard text.
3. Call `quote_order` to show price and delivery context.
4. Review the exact final text with the user, including line breaks.
5. Create a review link with `create_compose_link`, or create a hosted payment link with `create_payment_link`.
6. The user reviews and pays in PieterPost.
7. PieterPost prints and sends the mail after checkout succeeds.

## Direct Send

Use `create_direct_order` only for trusted API-credit workflows where the user explicitly wants direct sending.

For live direct-send calls:

- Require explicit confirmation.
- Use `confirmLiveSend=true`.
- Pass a reasonable `maxAmountCents`.
- Pass an `idempotencyKey`.

## Idempotency

Always pass an idempotency key when creating compose links, payment links, checkout links, top-ups, or direct orders. This prevents duplicate actions on retries.
