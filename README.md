# PixelWalls Payment Backend

This is the backend service for handling payments in the PixelWalls application using Razorpay.

## Setup

1. Create a `.env` file with your Razorpay credentials:
   ```
   RAZORPAY_KEY_ID=your_razorpay_key_id
   RAZORPAY_KEY_SECRET=your_razorpay_key_secret
   PORT=5000
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. For production:
   ```bash
   npm start
   ```

## API Endpoints

- `POST /create-order` - Create a new Razorpay order
- `POST /verify-payment` - Verify payment completion
- `GET /` - Health check endpoint

## Environment Variables

- `RAZORPAY_KEY_ID` - Your Razorpay key ID
- `RAZORPAY_KEY_SECRET` - Your Razorpay key secret
- `PORT` - Server port (default: 5000)

## Integration with Frontend

The frontend should make API calls to these endpoints to handle the payment flow:

1. Call `/create-order` when user selects a plan
2. Use the returned order details to initialize Razorpay checkout
3. Call `/verify-payment` to verify successful payments