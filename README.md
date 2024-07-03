# Paycard

Paycard is a peer-to-peer money transfer application that allows users to send money securely from one person to another. It features a dummy bank webhook server for facilitating secure transfers from a user's bank account to their wallet.

## Getting Started

Follow these steps to set up and run the project locally.

### Clone the Repository

```bash
git clone https://github.com/Bhavyabhardwaj/Paycard.git
cd Paycard
```

### Install Dependencies

```bash
npm install
```

### Set Up PostgreSQL

You can run PostgreSQL locally using Docker or use a cloud-based solution like Neon.tech.

```bash
docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
```

### Configure Environment Variables

Copy all `.env.example` files to `.env` and update them with the correct database URLs and other necessary configuration.

```bash
cp .env.example .env
```

### Database Setup

Navigate to the `packages/db` directory and run the following commands to set up the database:

```bash
cd packages/db
npx prisma migrate dev
npx prisma db seed
npx prisma generate
```

### Run the Application

Navigate to the `apps/user-app` directory and start the development server:

```bash
cd apps/user-app
npm run dev
```

### Logging In

You can log in using the following credentials (as defined in `seed.ts`):

- **Phone:** 1111111111
- **Password:** alice

## Contributing

We welcome contributions! Please fork the repository and submit pull requests.
