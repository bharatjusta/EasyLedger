# Shop Ledger Pro

A free, open-source single-page ledger application for small shops and businesses to track customer/vendor accounts, sales, and payments.

![Shop Ledger Pro](https://img.shields.io/badge/HTML5-CSS3--JS-orange) ![License](https://img.shields.io/badge/License-MIT-blue) ![No Dependencies](https://img.shields.io/badge/Dependencies-None-green)

## Features

- **Multi-Account Management** - Create unlimited customer/vendor accounts
- **Transaction Tracking** - Record sales (out) and payments (in) with dates and descriptions
- **Running Balance** - Automatic balance calculation per account
- **Due Date Tracking** - Set payment due dates with overdue highlighting
- **Search & Filter** - Search accounts and filter transactions by date range
- **Data Export** - Export to CSV for spreadsheets
- **Backup & Restore** - JSON backup with full data restore
- **Dark Mode** - Toggle between light and dark themes
- **Keyboard Shortcuts** - Fast navigation with keyboard controls
- **Print Support** - Print-friendly statement view
- **Offline Support** - Works offline with localStorage auto-save
- **Responsive Design** - Mobile-friendly interface

## Quick Start

1. **Download** the `ledger.html` file
2. **Open** it in any modern web browser (Chrome, Firefox, Edge, Safari)
3. **Start** by creating your first account

That's it! No installation, no dependencies, no server required.

## How to Use

### Creating Accounts
1. Enter an account name (e.g., customer name, supplier name)
2. Click "Create Account" or press Enter

### Adding Transactions
1. Select an account from the sidebar
2. Fill in the form:
   - **Date** - Transaction date
   - **Description** - What the transaction is for
   - **Sale (Out)** - Money you paid out (e.g., to suppliers)
   - **Payment (In)** - Money you received (e.g., from customers)
   - **Due Date** - Optional payment due date
3. Click "Add Entry" or press Enter

### Understanding Balance
- **Positive balance** = Customer owes you (they received goods but haven't paid fully)
- **Negative balance** = You owe the supplier (you received goods but haven't paid)
- Balance = Payments Received - Sales Made

### Saving Data
- **Desktop (Chrome/Edge)**: Uses File System Access API for auto-save
- **Mobile/Other browsers**: Data saves to browser localStorage automatically
- Use the **Backup** button for manual JSON backup

### Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| `Enter` | Add entry (in form) |
| `Ctrl+S` | Sync/Save |
| `Ctrl+B` | Open backup modal |
| `Ctrl+P` | Print statement |
| `Ctrl+D` | Toggle dark mode |
| `?` | Show shortcuts |
| `Esc` | Close modal |

## File Structure

```
shop-ledger/
├── ledger.html          # Main application (single file)
├── ledger-database.json # Data file (created on first save)
└── README.md           # This file
```

## Data Format

Data is stored in JSON format:
```json
{
  "accounts": [
    {
      "name": "Customer Name",
      "entries": [
        {
          "date": "2026-03-24",
          "desc": "Purchase order",
          "debit": 5000,
          "credit": 0,
          "dueDate": "2026-03-30"
        }
      ]
    }
  ]
}
```

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 86+ | Full (File System Access) |
| Edge 86+ | Full (File System Access) |
| Firefox | Full (localStorage only) |
| Safari | Full (localStorage only) |
| Mobile browsers | Full (localStorage only) |

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you find this useful, please consider:
- Starring the repository
- Sharing with others who might benefit
- Reporting issues or suggesting features

---

Made with simplicity in mind. No accounts, no cloud, no fees.
