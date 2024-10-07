# Integrating Passkey Authentication in a Next.js App using NextAuth and Hanko Passkey API

This repository demonstrates how to add passkey login functionality to your Next.js app using NextAuth and Hanko Passkey API. Passkey authentication is a secure and user-friendly alternative to traditional password-based authentication, providing a seamless login experience for users.

For a detailed tutorial on implementing passkey login in your Next.js app using NextAuth, refer to our blog post: [Add passkeys to your Next.js app using NextAuth](https://www.hanko.io/blog/passkeys-nextjs-nextauth)

![Passkey demo](/passkey.gif)

## Prerequisites

Before you begin, ensure you have the following:

- Node.js installed (version 20.0.0 or later)
- Hanko Passkey API key and tenant ID from [Hanko Cloud](https://cloud.hanko.io/)
- Resend API key from [Resend](https://resend.com/)
- DB URL. In this case we are using [Supabase](https://supabase.com/)

## Technologies used

- Next.js
- [Next-Auth](https://authjs.dev/) 
- [Resend](https://resend.com/)
- [Shadcn UI](https://ui.shadcn.com/)
- [Supabase](https://supabase.com/)
- [Prisma](https://www.prisma.io/)
- [Hanko Passkey API](https://www.hanko.io/features/hanko-passkey-api)

> **Note:**
> You'll need to create a Passkey Project on Hanko Cloud with the App URL `http://localhost:3000`. See our docs to learn how to setup a [passkey project](https://docs.hanko.io/passkey-api/setup-passkey-project).

## Getting started

1. Clone the repository

```bash
git clone https://github.com/teamhanko/passkeys-next-auth-starter.git
```

2. Set up environment variables

   * Create a `.env` file in the root directory and add the following environment variables:

    ```sh
    NEXTAUTH_SECRET=random-string
    NEXTAUTH_URL=http://localhost:3000

    GITHUB_ID=
    GITHUB_SECRET_ID=

    # for email service
    EMAIL_SERVER_USER=resend
    EMAIL_SERVER_PASSWORD=your-resend-api-key
    EMAIL_SERVER_HOST=smtp.resend.com
    EMAIL_SERVER_PORT=465
    EMAIL_FROM=onboarding@resend.dev

    DATABASE_URL=your-db-url

    PASSKEYS_API_KEY=your-hanko-passkey-api-key
    NEXT_PUBLIC_PASSKEYS_TENANT_ID=your-hanko-passkey-tenant-id
    ```

   * Replace `your-hanko-passkey-api-key` and `your-hanko-passkey-tenant-id` with your actual Hanko Passkey API key and tenant ID.

1. Install the dependencies using your preferred package manager (e.g., `npm`, `pnpm`, `yarn`, or `bun`). For this project, we've used `pnpm`:

```bash
pnpm install
```

4. Start the development server:

```bash
pnpm dev
```

## Usage

1. Start the application:

   - Access the application by navigating to `http://localhost:3000` in your web browser.

2. Sign up using email or GitHub.

3. Register a passkey:

   - After logging in, register a passkey for the logged-in user.

4. Log out:

   - After the passkey registration is successful, log out of the application.

5. Login with with a passkey

   - On the login page, choose sign in with a passkey option to authenticate using a passkey.

## Support

Feel free to reach out to us on [Discord](https://hanko.io/community) if you get into any issues.

## License

This project is licensed under the MIT License.

