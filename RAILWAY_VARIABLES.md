# Railway variables for this backend

Set these in the Railway service Variables page:

## Required

- `SPRING_DATASOURCE_URL` - JDBC MySQL URL, for example `jdbc:mysql://HOST:PORT/DATABASE`
- `SPRING_DATASOURCE_USERNAME` - MySQL username
- `SPRING_DATASOURCE_PASSWORD` - MySQL password
- `APP_JWT_SECRET` - a long random secret used to sign JWTs
- `APP_FRONTEND_RETURN_URL` - the frontend URL Paystack should return to after checkout
- `PAYSTACK_SECRET_KEY` - Paystack secret key
- `FIREBASE_DATABASE_URL` - Firebase Realtime Database URL if Firebase endpoints/features are used

## Optional

- `PAYSTACK_BASE_URL` - optional; defaults to `https://api.paystack.co`
- `PORT` - Railway normally supplies this automatically; the app defaults to `8080` locally

`APP_CALLBACK_BASE_URL` is no longer required because the application did not use it.

The backend does not need its own Railway public URL hardcoded in the source. Railway assigns the service domain externally. Point the Flutter/user and admin applications to that new domain.
