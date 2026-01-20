# Area51 Waitlist Landing Page

A sleek, futuristic landing page for Area51 with a dark, mysterious theme and neon accents.

## Features

- **Bold headline**: "Unlock the Unknown at Area51"
- **Subheadline**: "Join the waitlist and be the first to explore what lies beyond."
- **Email signup form**: Collect name and email from interested users
- **Live countdown timer**: Shows time remaining until launch (set to 30 days)
- **Dark theme with neon accents**: Black background with green and purple highlights
- **Fully responsive**: Mobile-friendly design
- **Call-to-action button**: Prominent "Join the Waitlist" button

## Usage

Simply open `index.html` in your web browser to view the landing page.

For web deployment, upload the `index.html` file to your web hosting service.

## Technologies

- Pure HTML5
- CSS3 with animations and gradients
- Vanilla JavaScript for countdown timer and form handling
- LocalStorage for storing waitlist entries (client-side demo)

## Customization

You can customize the countdown target date by modifying the JavaScript in `index.html`:

```javascript
// Change the number of days in the future
targetDate.setDate(targetDate.getDate() + 30);
```

For production use, replace the localStorage implementation with a proper backend API to store waitlist entries.