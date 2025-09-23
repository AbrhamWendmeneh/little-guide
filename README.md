# LittleGuide Email Verification Site

A standalone HTML page for handling email verification for the LittleGuide app using Supabase authentication.

## 🚀 Quick Deployment

### Option 1: Netlify (Recommended)

1. **Upload to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/your-username/littleguide-email-verification.git
   git push -u origin main
   ```

2. **Deploy on Netlify:**
   - Go to [Netlify](https://netlify.com)
   - Click "New site from Git"
   - Connect your GitHub repository
   - Set build command: `echo 'Static site'`
   - Set publish directory: `.`
   - Add environment variables in Site Settings > Environment Variables:
     - `SUPABASE_URL`: Your Supabase project URL
     - `SUPABASE_ANON_KEY`: Your Supabase anon key

### Option 2: Vercel

1. **Deploy with Vercel:**
   - Go to [Vercel](https://vercel.com)
   - Import your GitHub repository
   - Add environment variables:
     - `SUPABASE_URL`: Your Supabase project URL
     - `SUPABASE_ANON_KEY`: Your Supabase anon key

### Option 3: GitHub Pages

1. **Enable GitHub Pages:**
   - Go to repository Settings > Pages
   - Select "Deploy from a branch"
   - Choose `main` branch and `/` folder
   - Add environment variables in repository secrets (if supported)

## 🔧 Environment Variables

You need to set these environment variables in your deployment platform:

- `SUPABASE_URL`: Your Supabase project URL (e.g., `https://your-project.supabase.co`)
- `SUPABASE_ANON_KEY`: Your Supabase anon/public key

## 📝 Supabase Configuration

After deployment, update your Supabase project:

1. Go to Supabase Dashboard > Authentication > URL Configuration
2. Add your deployed URL to:
   - **Site URLs**: `https://your-deployed-url.netlify.app`
   - **Redirect URLs**: `https://your-deployed-url.netlify.app`

## 🎯 Features

- ✅ Secure environment variable configuration
- ✅ Automatic email verification
- ✅ Beautiful, responsive UI
- ✅ Error handling and user feedback
- ✅ Mobile-friendly design
- ✅ No hardcoded credentials

## 🔒 Security

- Uses environment variables for sensitive data
- No credentials exposed in the code
- Secure Supabase integration
- Proper error handling

## 📱 Usage

1. User signs up in your main app
2. Receives verification email from Supabase
3. Clicks verification link
4. Redirected to this verification page
5. Page automatically verifies the token
6. User sees success/error message
7. Can return to main app

## 🛠️ Customization

- Update the redirect URLs in the HTML file to match your main app
- Modify the styling in the `<style>` section
- Change the logo and branding as needed

## 📞 Support

For issues or questions, contact: support@littleguide.ai
