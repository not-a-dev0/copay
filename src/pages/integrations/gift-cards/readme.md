# Adding a New Gift Card

1. Ensure that the new gift card is included in the JSON response at https://bitpay.com/gift-cards/cards.
2. Ask a designer to provide a `cardImage`, `logo`, and `icon` for the new gift card, and save them in `assets/img/gift-cards/[brand]` with filenames `card.png`, `logo.svg`, and `icon.svg` respectively.
3. Add the new gift card to `providers/gift-card/offered-cards.ts` (Provide all fields required by the typescript types).

### Optional Adjustments

Gift card terms of use, description, and redeem instructions are automatically populated from https://bitpay.com/gift-cards/cards. However, you can override all 3 of them for any gift card by adding your overrides to the following components:

- Terms of Use: `pages/integrations/gift-cards/card-terms.html`
- Description: `pages/integrations/gift-cards/buy-card/card-description/card-description.html`
- Redeem Instructions: `pages/integrations/gift-cards/card-details/redeem-instructions/redeem-instructions.html`

### Troubleshooting

Is your card not showing up at https://bitpay.com/gift-cards/cards? The card might not be available in the country implied by your IP address. You can test which cards are available in specific countries by using a VPN.

### Testnet

To enable testnet mode, change `Network.livenet` to `Network.testnet` in `providers/gift-card/gift-card.ts`.
