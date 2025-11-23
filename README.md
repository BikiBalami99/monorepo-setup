## Monorepo Setup with AWS Amplify Next.js

This is a monorepo using Turborepo, pnpm workspaces, and AWS Amplify with Next.js (App Router).

## Structure

- `apps/web` - Next.js application with AWS Amplify
- `packages/` - Shared packages (for future use)
- `amplify/` - AWS Amplify backend configuration

## Features

- **Monorepo**: Using Turborepo for fast builds and caching
- **Package Manager**: pnpm workspaces for efficient dependency management
- **Authentication**: Setup with Amazon Cognito for secure user authentication
- **API**: Ready-to-use GraphQL endpoint with AWS AppSync
- **Database**: Real-time database powered by Amazon DynamoDB

## Getting Started

Install dependencies:

```bash
pnpm install
```

Run development server:

```bash
pnpm dev
```

Build all packages:

```bash
pnpm build
```

Build specific app:

```bash
pnpm turbo run build --filter=web
```

## Deploying to AWS

Configure AWS Amplify with:
- App root directory: `apps/web`
- The root `amplify.yml` will automatically handle the monorepo build process

For detailed instructions, refer to the [deployment section](https://docs.amplify.aws/nextjs/start/quickstart/nextjs-app-router-client-components/#deploy-a-fullstack-app-to-aws) of the AWS Amplify documentation.

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
