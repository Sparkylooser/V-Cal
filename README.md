# Vehicle Affordability Calculator

A modern, interactive web application that helps users determine whether they can realistically afford to purchase a vehicle based on their income and long-term ownership costs.

![Vehicle Affordability Calculator](https://img.shields.io/badge/React-18.x-blue) ![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3.x-38bdf8) ![Vite](https://img.shields.io/badge/Vite-5.x-646cff)

## 🚗 Overview

When purchasing a vehicle, the total financial burden extends beyond just the purchase price. This calculator evaluates affordability by considering financing costs, monthly ownership expenses, and your income to provide a clear recommendation.

### Key Features

- **Comprehensive Cost Analysis**: Calculates loan installments, fuel, insurance, and maintenance costs
- **Customizable Parameters**: Adjust interest rates, loan duration, down payment percentage, and affordability thresholds
- **Real-time Calculations**: Instant feedback on whether a vehicle fits your budget
- **User-Friendly Interface**: Clean, modern design with advanced settings toggle
- **Financial Guidelines**: Built-in 30% affordability rule (customizable) for sustainable long-term ownership

## 📊 How It Works

### Default Assumptions

1. **Down Payment**: 40% of vehicle price (customizable)
2. **Loan Terms**: 
   - Interest Rate: 15% per year (customizable)
   - Duration: 5 years (customizable)
3. **Monthly Ownership Costs**:
   - Fuel
   - Insurance
   - Maintenance
4. **Affordability Rule**: Total monthly vehicle costs should not exceed 30% of monthly income (customizable)

### Calculation Logic

The application:
1. Calculates the monthly loan installment using the standard amortization formula
2. Adds recurring monthly costs (fuel, insurance, maintenance)
3. Compares total monthly vehicle cost against your affordability threshold
4. Provides a clear verdict: **Affordable** or **Not Affordable**

### Formula

**Monthly Loan Payment** = L × [r(1 + r)^n] / [(1 + r)^n - 1]

Where:
- L = Loan amount (Vehicle Price - Down Payment)
- r = Monthly interest rate (Annual Rate / 12)
- n = Total number of payments (Years × 12)

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
```bash
   git clone https://github.com/yourusername/vehicle-affordability-calculator.git
   cd vehicle-affordability-calculator
```

2. **Install dependencies**
```bash
   npm install
```

3. **Start the development server**
```bash
   npm run dev
```

4. **Open your browser**
```
   Navigate to http://localhost:5173/
```

## 🛠️ Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool and dev server
- **Tailwind CSS 3** - Styling
- **Lucide React** - Icon library

## 📁 Project Structure
```
vehicle-calculator/
├── src/
│   ├── App.jsx          # Main calculator component
│   ├── index.css        # Tailwind CSS imports
│   └── main.jsx         # Application entry point
├── public/              # Static assets
├── index.html           # HTML template
├── package.json         # Dependencies and scripts
├── tailwind.config.js   # Tailwind configuration
├── postcss.config.js    # PostCSS configuration
└── vite.config.js       # Vite configuration
```

## 🎯 Usage

### Basic Usage

1. Enter the vehicle price
2. Enter your monthly income
3. Fill in estimated monthly costs (fuel, insurance, maintenance)
4. Click **Calculate**
5. Review the affordability verdict

### Advanced Settings

Click **Show Advanced Settings** to customize:
- **Interest Rate** (% per year)
- **Loan Duration** (years)
- **Down Payment** (% of vehicle price)
- **Affordability Threshold** (% of monthly income)

## 💡 Example Scenario

**Input:**
- Vehicle Price: LKR 1,200,000
- Monthly Income: LKR 100,000
- Fuel: LKR 15,000/month
- Insurance: LKR 5,000/month
- Maintenance: LKR 3,000/month
- Down Payment: 40%
- Interest Rate: 15%
- Loan Duration: 5 years

**Result:**
- Down Payment: LKR 480,000
- Loan Amount: LKR 720,000
- Monthly Installment: ~LKR 28,500
- Total Monthly Cost: ~LKR 51,500
- Affordability Limit (30%): LKR 30,000
- **Verdict**: Not Affordable (exceeds 30% threshold)

## 🔧 Available Scripts
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
```

## 🎨 Customization

### Changing Default Values

Edit the initial state values in `src/App.jsx`:
```javascript
const [vehiclePrice, setVehiclePrice] = useState(1200000);
const [monthlyIncome, setMonthlyIncome] = useState(50000);
const [interestRate, setInterestRate] = useState(15);
// ... and so on
```

### Styling

The application uses Tailwind CSS. Modify classes in `src/App.jsx` or extend the theme in `tailwind.config.js`.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact

Name - Rusiru

Project Link: [https://github.com/yourusername/vehicle-affordability-calculator](https://github.com/yourusername/vehicle-affordability-calculator)

## 🙏 Acknowledgments

- Design inspiration from modern financial calculators
- Built with React and Tailwind CSS
- Icons by [Lucide](https://lucide.dev/)

---

**Note**: This calculator provides estimates for educational purposes. Always consult with financial advisors for important purchasing decisions.
