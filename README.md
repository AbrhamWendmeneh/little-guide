# Little Guide Authentication Handler

This web page handles both email verification and password reset for the Little Guide app.

## Features

### Email Verification

- Handles email verification links from sign-up process
- Shows success/error states with appropriate messaging
- Redirects users back to the app after successful verification

### Password Reset

- Handles password reset links from forgot password flow
- Secure password reset form with validation
- Password strength requirements
- Confirmation matching
- Success confirmation after reset

## URL Parameters

### Email Verification

- `token`: Verification token from Supabase
- `type`: Usually "signup" for email verification
- `email`: User's email address

### Password Reset

- `type`: Set to "recovery" for password reset
- `access_token`: Supabase access token
- `refresh_token`: Supabase refresh token

## Password Requirements

- At least 8 characters long
- Contains at least one uppercase letter
- Contains at least one lowercase letter
- Contains at least one number

## Configuration

The page uses environment variables for Supabase configuration:

- `SUPABASE_URL`: Your Supabase project URL
- `SUPABASE_ANON_KEY`: Your Supabase anonymous key

## Deployment

This page is deployed to GitHub Pages at:
`https://AbrhamWendmeneh.github.io/little-guide/`

Make sure to update your Supabase project settings to include this URL in the allowed redirect URLs.

## Supabase Configuration

In your Supabase project dashboard:

1. Go to Authentication > URL Configuration
2. Add the following Site URLs:

   - `https://AbrhamWendmeneh.github.io/little-guide/`
   - `http://localhost:8081` (for development)

3. Add the following Redirect URLs:
   - `https://AbrhamWendmeneh.github.io/little-guide/`
   - `http://localhost:8081/auth-callback`

## Usage

### For Email Verification

Users will be redirected here automatically after clicking the verification link in their email.

### For Password Reset

Users will be redirected here after clicking the password reset link in their email. They can then enter a new password.

## Security

- All password operations are handled securely through Supabase
- Tokens are validated before allowing password changes
- Form validation prevents weak passwords
- CSRF protection through Supabase's built-in security
