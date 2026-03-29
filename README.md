# Ornique Data

Product catalog and asset repository for the **Ornique** jewelry store.

## Folder Structure

```
ornique-data/
├── assets/
│   └── jewelry/
│       ├── earrings/
│       ├── rings/
│       ├── bracelets/
│       ├── necklaces/
│       ├── hand-jewelry/
│       └── eye-jewelry/
├── data/
│   └── products.json
└── README.md
```

### `assets/jewelry/`

Static image assets organized by category. Each subfolder holds product images for its respective category.

| Folder          | Description                                       |
| --------------- | ------------------------------------------------- |
| `earrings/`     | Hoops, studs, danglers, jhumkas, threaders        |
| `rings/`        | Solitaires, bands, stackable sets, cocktail rings |
| `bracelets/`    | Charm, tennis, cuff, chain, bangle bracelets      |
| `necklaces/`    | Chokers, pendants, layered, lariat, bridal sets   |
| `hand-jewelry/` | Haath phool, finger chains, hand harnesses        |
| `eye-jewelry/`  | Brow bars, eye pins, temple chains, brow pieces   |

### `data/products.json`

JSON array containing **42 products** across 6 categories.

#### Product Schema

| Field              | Type       | Required | Description                            |
| ------------------ | ---------- | -------- | -------------------------------------- |
| `id`               | `number`   | Yes      | Unique product identifier              |
| `name`             | `string`   | Yes      | Product display name                   |
| `category`         | `string`   | Yes      | One of the 6 categories listed below   |
| `price`            | `number`   | Yes      | Current selling price (INR)            |
| `original_price`   | `number`   | No       | Price before discount                  |
| `discounted_price` | `number`   | No       | Price after discount (same as `price`) |
| `discount_percent` | `number`   | No       | Discount percentage (19–30%)           |
| `description`      | `string`   | Yes      | Short product description              |
| `featured`         | `boolean`  | Yes      | Whether the product is featured        |
| `images`           | `string[]` | Yes      | Array of image URLs (1–2 per product)  |
