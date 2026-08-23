# Armoniq Storefront

[![Quality gate status](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Bugs](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=bugs)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Code Smells](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=code_smells)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Coverage](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=coverage)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=security_rating)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront) [![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=CodeInTheIzzyverse_Armoniq-storefront&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=CodeInTheIzzyverse_Armoniq-storefront)

> Customer-facing ecommerce website for Armoniq, a fictional music store offering instruments, studio equipment, accessories, and other music-related products.

**Status:** In Development  
**Platform:** Web Application  
**Language:** TypeScript  
**Repository:** [GitHub](https://github.com/Isa-Bedoya-UdeA/Armoniq-storefront)

## Overview

Armoniq Storefront is the public ecommerce application of the Armoniq project.

Customers can browse musical instruments and music-related equipment, search and filter products, view product details, write reviews, manage favorites and carts, authenticate, manage addresses, checkout, make test payments through Wompi Sandbox, view orders, and read the store blog.

The Storefront is an independent Next.js application that communicates with the Armoniq API for all business operations.

## Features

- Responsive homepage.
- Promotional home slides.
- Featured products.
- Product categories and subcategories.
- Product search.
- Product filtering by category, subcategory, rating, and price range.
- Product sorting and pagination.
- Product details and image galleries.
- Product ratings and reviews.
- Customer registration and login.
- Email verification.
- Password recovery and reset.
- Favorites.
- Shopping cart.
- Customer account.
- Order history and order details.
- Order status and tracking information.
- Address CRUD.
- Google Maps-assisted address selection.
- Cash-on-delivery checkout.
- Wompi Sandbox checkout.
- Blog listing and post pages.
- Contact page.
- Responsive mobile-first UX.
- Loading, empty, error, and success states.
- Automated frontend testing.

## Tech Stack

| Category | Technology |
| --- | --- |
| Framework | ![Next JS](https://img.shields.io/badge/Next-black.svg?style=for-the-badge&logo=next.js&logoColor=white) |
| UI Library | ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) |
| Language | ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) |
| Package Manager | ![PNPM](https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220) |
| Styling | ![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white) |
| HTTP Client | Axios |
| Server State | TanStack Query |
| Client State | Zustand |
| Forms | ![React Hook Form](https://img.shields.io/badge/React%20Hook%20Form-%23EC5990.svg?style=for-the-badge&logo=reacthookform&logoColor=white) |
| Validation | ![Zod](https://img.shields.io/badge/zod-%233068b7.svg?style=for-the-badge&logo=zod&logoColor=white) |
| Icons | Lucide React |
| Date Utilities | date-fns |
| Carousel | Embla Carousel |
| Maps | `@vis.gl/react-google-maps` |
| Unit/Component Testing | ![Vitest](https://img.shields.io/badge/-Vitest-252529?style=for-the-badge&logo=vitest&logoColor=FCC72B) |
| Component Testing | ![Testing Library](https://img.shields.io/badge/-TestingLibrary-%23E33332?style=for-the-badge&logo=testing-library&logoColor=white) |
| E2E Testing | Playwright |
| Code Quality | [ESLint](https://img.shields.io/badge/ESLint-4B3263?style=for-the-badge&logo=eslint&logoColor=white) + ![Prettier](https://img.shields.io/badge/prettier-%23192a32?style=for-the-badge&logo=prettier&logoColor=dc524a) |
| Git Hooks | Husky + lint-staged + Commitlint |
| Code Analysis | ![SonarQube](https://img.shields.io/badge/sonarqube-%23126ED3.svg?style=for-the-badge&logo=sonarqubecloud&logoColor=white) |
| CI/CD | ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) |
| Deployment | ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white) |

## Architecture

The Storefront follows a **feature-oriented frontend architecture using the Next.js App Router**.

The application separates:

- App routes and pages.
- Layout components.
- Feature components.
- Reusable UI components.
- Hooks.
- API/service integration.
- Server state.
- Client state.
- Types.
- Constants.
- Utilities.
- SCSS styles.
- Tests.

Detailed architectural decisions are documented in [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md).

## Project Structure

```text
app/
├── (auth)/
│   ├── forgot-password/
│   ├── login/
│   ├── register/
│   ├── reset-password/
│   └── verify-email/
├── (store)/
│   ├── blog/
│   ├── cart/
│   ├── categories/
│   ├── checkout/
│   ├── contact/
│   ├── favorites/
│   ├── products/
│   └── search/
├── account/
├── error.tsx
├── layout.tsx
├── loading.tsx
├── not-found.tsx
└── page.tsx

components/
├── Features/
├── Layout/
└── UI/

constants/
hooks/
lib/
public/
services/
store/
styles/
tests/
types/
docs/
```

## Getting Started

### Prerequisites

Install:

- Node.js LTS.
- pnpm.
- Git.

The Storefront also requires access to a running/deployed Armoniq API.

### Clone the Repository

```bash
git clone https://github.com/Isa-Bedoya-UdeA/Armoniq-storefront.git
cd Armoniq-storefront
```

### Install Dependencies

```bash
pnpm install
```

### Configure Environment Variables

```bash
cp .env.example .env.local
```

On Windows PowerShell:

```powershell
Copy-Item .env.example .env.local
```

Never commit real credentials.

Relevant integrations include:

- Armoniq API.
- Google Maps.
- Wompi Sandbox.

For backend-related configuration, consult the API documentation:

- [`docs/API.md`](https://github.com/Isa-Bedoya-UdeA/Armoniq-api/blob/main/docs/API.md)
- [`docs/AUTHENTICATION.md`](https://github.com/Isa-Bedoya-UdeA/Armoniq-api/blob/main/docs/AUTHENTICATION.md)
- [`docs/SECURITY.md`](https://github.com/Isa-Bedoya-UdeA/Armoniq-api/blob/main/docs/SECURITY.md)
- [`docs/DEPLOYMENT.md`](https://github.com/Isa-Bedoya-UdeA/Armoniq-api/blob/main/docs/DEPLOYMENT.md)

### Run the Application

Development:

```bash
pnpm dev
```

Production:

```bash
pnpm build
pnpm start
```

## Documentation

| Document | Description |
| --- | --- |
| [`SPEC.md`](SPEC.md) | Product and technical specification |
| [`docs/REQUIREMENTS.md`](docs/REQUIREMENTS.md) | Functional and non-functional requirements |
| [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) | Frontend architecture and design decisions |
| [`docs/TESTING.md`](docs/TESTING.md) | Testing strategy |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution and development workflow |
| [`LICENSE`](LICENSE) | MIT license |

Backend documentation is maintained in the API repository.

## Screenshots

### Home

![Home desktop](docs/assets/screenshots/home-desktop.png)

![Home mobile](docs/assets/screenshots/home-mobile.png)

### Product Catalog

![Product catalog desktop](docs/assets/screenshots/catalog-desktop.png)

![Product catalog mobile](docs/assets/screenshots/catalog-mobile.png)

### Product Details

![Product details desktop](docs/assets/screenshots/product-details-desktop.png)

![Product details mobile](docs/assets/screenshots/product-details-mobile.png)

### Cart and Checkout

![Cart desktop](docs/assets/screenshots/cart-desktop.png)

![Checkout mobile](docs/assets/screenshots/checkout-mobile.png)

### Customer Account

![Account desktop](docs/assets/screenshots/account-desktop.png)

![Orders mobile](docs/assets/screenshots/orders-mobile.png)

> Screenshots are placeholders and should be replaced with real captures as development progresses.

## Demo

Store the Storefront demo video under:

```text
docs/assets/demo/
```

Example:

![Storefront demo](docs/assets/demo/storefront-demo.mp4)

## Development

Development is managed through GitHub using:

- Source control.
- Issues.
- Milestones.
- Pull Requests.
- Releases when appropriate.
- GitHub Actions.
- SonarCloud.

Design and documentation tooling includes:

- Figma for palettes, typography, logos, UI design, and visual assets.
- Lucidchart for database and architecture diagrams.

Development principles include:

- SOLID.
- Separation of Concerns.
- Reusable UI components.
- DRY where appropriate.
- KISS where appropriate.
- Mobile-first responsive design.
- Accessibility.
- Typed API contracts.
- Consistent SCSS architecture.
- Reusable hooks and services.
- Clear separation of server and client state.

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Testing

The Storefront uses:

- Vitest.
- Testing Library.
- Testing Library DOM matchers.
- Testing Library User Event.
- Playwright.

Testing should cover:

- UI components.
- Forms.
- Authentication.
- Product catalog.
- Product details.
- Reviews.
- Favorites.
- Cart.
- Checkout.
- Customer account.
- Addresses.
- Critical navigation and ecommerce journeys.

Typical checks:

```bash
pnpm lint
pnpm test
pnpm build
```

Critical customer journeys should have Playwright E2E coverage.

## CI/CD

GitHub Actions should validate:

1. Dependency installation.
2. Linting.
3. Type checking.
4. Unit/component tests.
5. Production build.
6. E2E tests where configured.
7. Quality checks where configured.

The Storefront is independently deployed from the Admin and API.

## Security and Privacy

The Storefront must not expose private backend credentials, database credentials, Cloudinary secrets, Wompi private credentials, or other server-side secrets.

Authentication is handled through the API's secure access/refresh-token architecture.

Google Maps configuration must follow the provider's frontend API-key restrictions and never expose server-side credentials.

## Performance

The Storefront prioritizes:

- Mobile-first rendering.
- Optimized images.
- Cloudinary image transformations.
- Efficient API requests.
- TanStack Query caching.
- Lazy loading where appropriate.
- Minimal unnecessary client-side JavaScript.
- Good Core Web Vitals.

The application is designed for free-tier infrastructure and portfolio traffic.

## SEO and Accessibility

The Storefront uses Next.js metadata capabilities for appropriate:

- Page titles.
- Descriptions.
- Open Graph metadata.
- Product metadata.
- Blog metadata.

Accessibility includes:

- Semantic HTML.
- Keyboard navigation.
- Visible focus states.
- Form labels.
- Accessible controls.
- Clear validation feedback.
- Loading and error states.

## Deployment

The Storefront is intended to be independently deployed on Vercel.

Deployment configuration and environment requirements are documented in the project documentation and the API repository.

The project uses free-tier and sandbox services suitable for portfolio development.

## License

This project is licensed under the MIT License.

See [`LICENSE`](LICENSE).

## Contributors

Developed by **Isabela Bedoya Gaviria**.
