# Karamachedu Village Survey Application

A comprehensive survey application designed to help the village of Karamachedu in Andhra Pradesh, India, identify and address the needs of below poverty line families for government schemes in Education, Health, and Elder Care.

## Features

### 📝 Survey Form
- **Multi-step form** with 5 comprehensive sections
- **Basic Information**: Family details, contact information, BPL card numbers
- **Family Composition**: Total members, children, elderly, disabled members
- **Education Details**: School attendance, dropout rates, scheme awareness
- **Health Information**: Insurance coverage, chronic diseases, healthcare access
- **Elder Care**: Pension status, care needs, scheme utilization
- **Employment & Income**: Occupation, monthly income, employment schemes
- **Bank Details**: Financial inclusion information

### 📋 Survey Data Management
- **Data listing** with search and filtering capabilities
- **Pagination** for large datasets
- **Status tracking** (Surveyed, Under Review, Assistance Provided, Follow-up Required)
- **Priority levels** (High, Medium, Low) for government assistance

### 📊 Summary Reports
- **Comprehensive statistics** and analytics
- **Visual charts** for education, health, and elder care needs
- **Progress tracking** for scheme awareness and utilization
- **Priority distribution** analysis
- **Key recommendations** for government intervention

### 🔐 Authentication
- **Google OAuth** integration for secure access
- **User session management**
- **Role-based access control**

## Technology Stack

- **Frontend**: Next.js 15, React 18
- **Backend**: Next.js API Routes
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: NextAuth.js with Google Provider
- **Styling**: CSS Modules with responsive design

## Prerequisites

- Node.js 18+ 
- MongoDB (local or Atlas)
- Google OAuth credentials

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd karamchedu-survey
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   ```env
   # NextAuth Configuration
   NEXTAUTH_SECRET=your-nextauth-secret-key-here
   NEXTAUTH_URL=http://localhost:3000

   # Google OAuth (for authentication)
   GOOGLE_ID=your-google-client-id
   GOOGLE_SECRET=your-google-client-secret

   # MongoDB Connection
   MONGODB_URI=mongodb://localhost:27017/KaramChedu
   # Or for MongoDB Atlas:
   # MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/KaramChedu?retryWrites=true&w=majority
   ```

4. **Set up Google OAuth**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select existing one
   - Enable Google+ API
   - Create OAuth 2.0 credentials
   - Add authorized redirect URI: `http://localhost:3000/api/auth/callback/google`
   - Copy Client ID and Client Secret to your `.env.local`

5. **Set up MongoDB**
   - **Local MongoDB**: Install and start MongoDB service
   - **MongoDB Atlas**: Create a free cluster and get connection string

6. **Run the development server**
   ```bash
   npm run dev
   ```

7. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## Usage

### Authentication
1. Click "Sign in with Google" on the login page
2. Authorize the application with your Google account
3. You'll be redirected to the main application

### Survey Data Collection
1. Navigate to the "Survey Form" tab
2. Fill out the 5-step form with family information
3. Submit the form to save data to MongoDB
4. Form automatically resets for the next family

### Data Management
1. Go to "Survey Data" tab to view all submissions
2. Use search and filters to find specific families
3. View family details, priority levels, and status
4. Navigate through pages for large datasets

### Summary Reports
1. Access "Summary Report" tab for analytics
2. View key statistics and visualizations
3. Analyze education, health, and elder care needs
4. Review recommendations for government intervention

## Database Schema

The application uses a comprehensive MongoDB schema (`SurveyInfo` collection in `KaramChedu` database) with the following key sections:

### Basic Information
- Family name, head of family, contact details
- BPL card number, Aadhar number
- Complete address

### Family Composition
- Total family members
- Children under 18, elderly above 60
- Disabled members count

### Education Details
- Children in school vs dropped out
- Education scheme awareness and utilization
- Specific education needs (fees, books, uniforms, etc.)

### Health Information
- Health insurance coverage and type
- Chronic diseases and medication needs
- Healthcare facility access
- Health scheme awareness and utilization

### Elder Care
- Elderly care requirements
- Pension status and amounts
- Elder care scheme utilization

### Employment & Financial
- Primary occupation and monthly income
- Employment scheme awareness
- Bank account details and financial inclusion

## API Endpoints

### Survey Data
- `POST /api/survey` - Submit new survey data
- `GET /api/survey` - Retrieve survey data with pagination and filters

### Summary Statistics
- `GET /api/survey-summary` - Get comprehensive analytics and statistics

## Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically

### Other Platforms
- **Netlify**: Similar to Vercel deployment
- **Railway**: Supports Node.js and MongoDB
- **Heroku**: Add MongoDB add-on

### Environment Variables for Production
```env
NEXTAUTH_SECRET=your-production-secret
NEXTAUTH_URL=https://your-domain.com
GOOGLE_ID=your-google-client-id
GOOGLE_SECRET=your-google-client-secret
MONGODB_URI=your-production-mongodb-uri
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions:
- Create an issue in the repository
- Contact the development team

## Acknowledgments

- Built for the village of Karamachedu, Andhra Pradesh, India
- Designed to help below poverty line families access government schemes
- Focus on Education, Health, and Elder Care support
#   K a r a m C h e d u  
 