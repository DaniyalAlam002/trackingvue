# FitLife Gym Booking Website

A modern, responsive gym booking website built with Vue.js 3, Vite, Vue Router, and TailwindCSS.

## Features

- **Home Page**: Hero section with strong CTA, newsletter subscription, and contact form
- **Booking Page**: Comprehensive booking form with all input types and modal for previous gym experience
- **About Page**: Gym information, trainer details, and facility overview
- **Responsive Design**: Mobile-friendly interface with modern UI/UX
- **Smooth Transitions**: Modal animations and hover effects
- **Reusable Components**: Header, Footer, and Modal components

## Tech Stack

- **Frontend Framework**: Vue.js 3 with Composition API
- **Build Tool**: Vite
- **Routing**: Vue Router 4
- **Styling**: TailwindCSS
- **Icons**: Heroicons (SVG)
- **Fonts**: Inter (Google Fonts)

## Project Structure

```
tracking-site-vue/
├── src/
│   ├── components/
│   │   ├── Header.vue          # Navigation header with phone number
│   │   ├── Footer.vue          # Footer with contact information
│   │   └── Modal.vue           # Reusable modal component
│   ├── views/
│   │   ├── Home.vue            # Home page with hero and sections
│   │   ├── Booking.vue         # Booking form with all input types
│   │   └── About.vue           # About page with gym information
│   ├── router/
│   │   └── index.js            # Vue Router configuration
│   ├── App.vue                 # Main app component
│   ├── main.js                 # App entry point
│   └── style.css               # Global styles and TailwindCSS
├── index.html                  # HTML template
├── package.json                # Dependencies and scripts
├── vite.config.js             # Vite configuration
├── tailwind.config.js         # TailwindCSS configuration
├── postcss.config.js          # PostCSS configuration
└── README.md                  # Project documentation
```

## Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd tracking-site-vue
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Key Features Implementation

### 1. Home Page (/)
- **Hero Section**: Eye-catching gradient background with CTA button
- **Phone Number Display**: Prominently featured in header, hero, and footer
- **Newsletter Subscription**: Email input with validation (no form tag)
- **Contact Section**: Name, phone, message inputs (no form tag)
- **Features Section**: Three-column grid highlighting gym benefits

### 2. Booking Page (/book)
- **Comprehensive Form**: Includes all common input types:
  - Text, email, password, tel, number, date, time
  - File upload, textarea, select dropdown
  - Checkboxes, radio buttons
- **Previous Experience Modal**: Popup form for gym experience details
- **Form Validation**: Required field validation and user feedback
- **Booking Summary**: Displays captured data after form submission

### 3. About Page (/about)
- **Gym Story**: Company history and mission
- **Trainer Profiles**: Expert trainer information and certifications
- **Facility Overview**: Equipment and amenities details
- **Contact Information**: Multiple ways to reach the gym
- **CTAs**: Multiple buttons linking back to booking page

### 4. Reusable Components

#### Header.vue
- Responsive navigation with mobile menu
- Gym phone number display
- Active route highlighting

#### Footer.vue
- Contact information and quick links
- Gym phone number and address
- Social media and company details

#### Modal.vue
- Smooth open/close transitions
- Backdrop click to close
- Customizable title and confirm text
- Slot-based content injection

## Styling & Design

### TailwindCSS Configuration
- Custom color palette with primary and secondary colors
- Responsive breakpoints for mobile-first design
- Custom animations and transitions
- Component-based utility classes

### Responsive Design
- Mobile-first approach
- Grid layouts that adapt to screen size
- Touch-friendly buttons and inputs
- Optimized typography for all devices

### UI Components
- Custom button styles with hover effects
- Form input styling with focus states
- Card components with shadows and hover effects
- Consistent spacing and typography

## Form Features

### Input Types Covered
- **Text Inputs**: Name, comments, medical info
- **Email**: Email address with validation
- **Password**: Secure password input
- **Telephone**: Phone number input
- **Number**: Age, weight with min/max values
- **Date**: Preferred session date with minimum date validation
- **Time**: Preferred session time
- **File Upload**: Profile picture upload
- **Textarea**: Multi-line text input
- **Select**: Dropdown for duration and training type
- **Checkboxes**: Multiple fitness goals selection
- **Radio Buttons**: Fitness level selection

### Form Validation
- Required field validation
- Email format validation
- Date range validation
- User feedback messages
- Form submission handling

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance Features

- **Code Splitting**: Route-based code splitting with Vue Router
- **Optimized Builds**: Vite for fast development and optimized production builds
- **CSS Optimization**: TailwindCSS purging for minimal CSS output
- **Lazy Loading**: Components loaded only when needed

## Development Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## Customization

### Colors
Edit `tailwind.config.js` to modify the color scheme:
```javascript
colors: {
  primary: {
    50: '#f0f9ff',
    // ... customize primary colors
  },
  secondary: {
    // ... customize secondary colors
  }
}
```

### Content
- Update gym information in component files
- Modify phone numbers and contact details
- Customize trainer profiles and facility descriptions

### Styling
- Modify component classes in Vue files
- Update global styles in `style.css`
- Customize TailwindCSS configuration

## Deployment

### Build the Project
```bash
npm run build
```

### Deploy to Static Hosting
The built files in the `dist` folder can be deployed to:
- Netlify
- Vercel
- GitHub Pages
- AWS S3
- Any static hosting service

### Environment Variables
No environment variables are required for basic functionality. For production, consider adding:
- Analytics tracking IDs
- Contact form endpoints
- Newsletter subscription service

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For questions or support, please contact:
- Phone: (555) 123-4567
- Email: info@fitlifegym.com

---

**Built with ❤️ using Vue.js 3, Vite, and TailwindCSS**
