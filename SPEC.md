# Armoniq Storefront Specification

> **Project:** Armoniq  
> **Repository:** `storefront`  
> **Application type:** Customer-facing ecommerce web application  
> **Stack:** Next.js, React, TypeScript, SCSS, pnpm

## 1. Overview

Armoniq Storefront is the public customer-facing ecommerce website for the fictional Armoniq music store.

Customers can browse musical instruments and music-related equipment, search and filter the catalog, view product details, review products, manage favorites and carts, authenticate, checkout, manage addresses, and track their orders.

The Storefront is an independent Next.js application that communicates exclusively with the Armoniq API for business operations.

## 2. Product Vision

Provide a polished, realistic, responsive ecommerce experience that demonstrates professional frontend development while remaining suitable for a portfolio project.

The Storefront should feel like a real online music store rather than a simple CRUD demonstration.

It must prioritize:

- Strong visual hierarchy.
- Responsive mobile-first design.
- Fast navigation.
- Accessible interactions.
- Clear ecommerce flows.
- Reusable components.
- Reliable API integration.
- Good loading and error handling.
- Secure authentication behavior.
- Automated testing.

## 3. Functional Overview

Customers must be able to:

- Browse featured products.
- Browse categories.
- Browse subcategories.
- Search products.
- Filter by category.
- Filter by subcategory.
- Filter by rating.
- Filter by minimum price.
- Filter by maximum price.
- Sort products.
- Paginate product results.
- View product details.
- View product images.
- View ratings and reviews.
- Create product reviews when authorized.
- Add products to favorites.
- Remove products from favorites.
- View favorites.
- Add products to the cart.
- Update cart quantities.
- Remove cart items.
- Register.
- Log in.
- Verify email.
- Recover a password.
- Reset a password.
- Manage their customer account.
- Manage saved addresses.
- Select an address using map functionality.
- Checkout.
- Pay using cash on delivery.
- Pay using Wompi Sandbox.
- View orders.
- View order details.
- View order status.
- View tracking numbers when available.
- Read the Armoniq blog.
- Contact the store.
- View relevant store information.

## 4. Core Features

### 4.1 Global Layout

Implement:

- Header.
- Footer.
- Responsive navigation.
- Global search.
- Authentication access.
- Favorites access.
- Cart access.
- Store branding.

Branding must be retrieved from the API where appropriate.

### 4.2 Home Page

The homepage must include appropriate sections such as:

- Hero/home slides.
- Featured products.
- Categories.
- Promotional banners.
- Blog highlights.
- Other relevant promotional content.

Slides and banners must be managed by the Admin application and delivered through the API.

### 4.3 Product Catalog

Implement:

- Product listing.
- Search.
- Category filters.
- Subcategory filters.
- Rating filters.
- Minimum price.
- Maximum price.
- Sorting.
- Pagination.
- Loading states.
- Empty states.
- Error states.

### 4.4 Product Details

The product details page must display:

- Product name.
- Product images.
- Description.
- Price.
- Availability.
- Rating.
- Review count.
- Rating distribution.
- Reviews.
- Quantity selector.
- Add-to-cart action.
- Favorite action.

### 4.5 Reviews and Ratings

Authenticated customers must be able to:

- Rate products.
- Create reviews.
- Edit their own reviews.
- Delete their own reviews where permitted.

The Storefront must display:

- Average rating.
- Rating distribution.
- Review count.
- Individual reviews.

### 4.6 Authentication

Implement:

- Login.
- Registration.
- Email verification.
- Forgot password.
- Reset password.
- Session handling.
- Logout.
- Protected customer routes.

Authentication must work with the API's access/refresh token architecture.

### 4.7 Favorites

Implement:

- Add favorite.
- Remove favorite.
- Favorites listing.
- Empty state.
- Product actions from favorites.

### 4.8 Shopping Cart

Implement:

- Cart listing.
- Quantity updates.
- Item deletion.
- Cart totals.
- Product availability handling.
- Price-change handling.
- Checkout navigation.

The cart must be synchronized with backend validation before order creation.

### 4.9 Checkout

The checkout must include:

- Customer information.
- Address selection.
- Address creation.
- Order summary.
- Payment method selection.
- Order validation.
- Payment initialization.
- Payment result handling.

Supported payment methods:

- Cash on delivery.
- Wompi Sandbox.

### 4.10 Customer Account

Implement:

- Account dashboard.
- Profile information.
- Order history.
- Order details.
- Order status.
- Payment status.
- Tracking information.
- Address CRUD.
- Default address.
- Favorites.

### 4.11 Google Maps Address Selection

Use Google Maps Platform to provide map-assisted address selection.

The feature should support:

- Location selection.
- Latitude and longitude.
- Address information.
- Integration with saved customer addresses.

Sensitive Google credentials must not be exposed.

### 4.12 Blog

Implement:

- Blog listing.
- Blog post details.
- Cover images.
- Post metadata.
- Published content.
- Related posts where appropriate.

Only published content should be publicly accessible.

### 4.13 Contact

Implement a contact page with:

- Store information.
- Contact information.
- Relevant social links.
- Appropriate contact functionality.

## 5. Requirements

Functional and non-functional requirements are defined in:

- [`docs/REQUIREMENTS.md`](docs/REQUIREMENTS.md)

The Storefront must comply with those requirements.

## 6. MVP

The MVP includes:

- Responsive global layout.
- Homepage.
- Product catalog.
- Product search.
- Product filtering.
- Product details.
- Product ratings/reviews.
- Registration.
- Login.
- Email verification.
- Password recovery.
- Favorites.
- Shopping cart.
- Customer account.
- Address CRUD.
- Google Maps address selection.
- Checkout.
- Cash on delivery.
- Wompi Sandbox.
- Order history.
- Order details.
- Tracking information.
- Blog listing and posts.
- Contact page.
- API integration.
- Unit/component tests.
- E2E tests for critical flows.
- CI/CD.
- Vercel deployment.

## 7. Important Features

If time allows, prioritize:

- Advanced product filtering.
- Improved product search.
- Product recommendations.
- Recently viewed products.
- Rich product image gallery.
- Optimistic UI for favorites/cart where safe.
- Advanced checkout validation.
- Better account dashboard.
- Improved blog navigation.
- SEO metadata.
- Performance optimization.

## 8. Stretch Features

Optional enhancements:

- Product comparison.
- Product variants.
- Wishlist improvements.
- Coupon system.
- Gift cards.
- Product recommendations.
- Recently viewed products.
- Customer notifications.
- Multiple currencies.
- Multiple languages.
- Advanced search.
- Reviews with media.
- Back-in-stock notifications.
- Loyalty features.

## 9. Out of Scope

- Direct database access.
- Direct access to Cloudinary private credentials.
- Direct access to payment-provider secrets.
- Microservices.
- Kubernetes.
- Enterprise infrastructure.
- Arbitrary theme customization.
- Customer-controlled global palette customization.
- Unrelated social networking features.
- Real production payment processing.
- Real commercial operation.
- Full marketplace functionality for third-party sellers.

## 10. Constraints

- Next.js + React + TypeScript.
- pnpm only.
- SCSS only.
- No Tailwind CSS.
- Mobile-first responsive design.
- Reusable UI and feature components.
- App Router.
- API communication through Axios.
- TanStack Query for server state.
- Zustand for suitable client state.
- React Hook Form and Zod for forms.
- Google Maps through `@vis.gl/react-google-maps`.
- Wompi Sandbox for payment testing.
- Authentication must use the API's secure token architecture.
- Sensitive environment variables must never be exposed.
- `.env.example` must be included.
- All services must remain within free-tier or sandbox limits.
- Testing must use Vitest, Testing Library, and Playwright.
- CI/CD must use GitHub Actions.
- Planned deployment platform: Vercel.

## 11. Technology Stack

- Next.js.
- React.
- TypeScript.
- SCSS.
- Axios.
- Zustand.
- TanStack Query.
- React Hook Form.
- Zod.
- Lucide React.
- date-fns.
- Embla Carousel.
- `@vis.gl/react-google-maps`.
- Vitest.
- Testing Library.
- Playwright.
- GitHub Actions.
- Vercel.

## 12. Frontend Architecture Principles

The application must maintain separation between:

- App routes/pages.
- Layout components.
- Feature components.
- UI components.
- Hooks.
- API services.
- Client state.
- Server state.
- Types.
- Constants.
- Utilities.
- Styles.
- Tests.

The intended structure includes:

- `app/` for routes and pages.
- `components/` for reusable UI and feature components.
- `hooks/` for reusable React hooks.
- `services/` for API/service integration.
- `store/` for client state.
- `types/` for TypeScript types.
- `constants/` for application constants.
- `lib/` for reusable utilities and validation helpers.
- `styles/` for global SCSS architecture.
- `tests/` for frontend tests.

## 13. SCSS Architecture

Styling must be implemented entirely with SCSS.

The styling system must include reusable:

- Variables.
- Mixins.
- Responsive breakpoints.
- Utilities.
- Global styles.
- Component/page styles.

The responsive mixin must provide a consistent way to handle screen sizes, such as a `respond-to` mixin.

Tailwind CSS and plain CSS files must not be introduced as an alternative styling system.

## 14. UX and Accessibility

The Storefront must provide:

- Mobile-first responsive design.
- Semantic HTML.
- Keyboard navigation.
- Visible focus states.
- Accessible forms.
- Accessible dialogs.
- Proper labels.
- Accessible interactive controls.
- Clear validation messages.
- Loading states.
- Empty states.
- Error states.
- Success feedback.
- Confirmation where destructive actions require it.

The ecommerce flow must remain usable on mobile devices.

## 15. Performance

The application should prioritize:

- Optimized images.
- Appropriate Next.js image handling.
- Cloudinary transformations where applicable.
- Efficient API requests.
- TanStack Query caching.
- Request deduplication.
- Appropriate lazy loading.
- Minimal client-side JavaScript where possible.
- Good Core Web Vitals.

The project should load quickly enough for portfolio visitors using free-tier infrastructure.

## 16. SEO

The Storefront should use Next.js metadata capabilities for:

- Page titles.
- Descriptions.
- Open Graph metadata.
- Product metadata where applicable.
- Blog metadata.
- Appropriate canonical URLs where applicable.

Advanced SEO automation is not required for the MVP.

## 17. Testing

Frontend testing must use:

- Vitest.
- Testing Library.
- Testing Library Jest DOM.
- Testing Library User Event.
- Playwright.

Testing should cover:

- UI components.
- Forms.
- Authentication.
- Product catalog.
- Product details.
- Cart.
- Favorites.
- Checkout.
- Account.
- Critical navigation flows.

Critical customer journeys must have E2E coverage.

## 18. CI/CD

GitHub Actions must run:

- Dependency installation.
- Linting.
- Type checking.
- Unit/component tests.
- Production build.
- E2E tests where appropriate.

The application must be independently deployable from the Admin and API repositories.

## 19. Definition of Done

A Storefront feature is complete when:

- UI is implemented.
- API integration works.
- Loading, error, empty, and success states exist.
- Forms are validated.
- Authentication/authorization behavior is respected.
- Responsive behavior is verified.
- Accessibility considerations are addressed.
- Relevant automated tests exist.
- Critical flows have E2E coverage.
- Documentation is updated when necessary.
- ESLint passes.
- TypeScript checks pass.
- Tests pass.
- Production build succeeds.
- CI checks pass.

## 20. Documentation References

- [`docs/REQUIREMENTS.md`](docs/REQUIREMENTS.md)
- [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md)
- [`docs/TESTING.md`](docs/TESTING.md)

The API repository is the authoritative source for backend API behavior, authentication, database, security, payment, and external integration specifications.

## 21. Project Success Criteria

The Storefront is successful when a visitor can experience a complete ecommerce workflow:

1. Visit the homepage.
2. Browse the catalog.
3. Search and filter products.
4. View a product.
5. Register or log in.
6. Add products to favorites.
7. Add products to the cart.
8. Manage an address.
9. Select an address using the map.
10. Checkout.
11. Select cash on delivery or Wompi Sandbox.
12. Complete the payment/test flow.
13. View the resulting order.
14. Track its status and tracking number.
15. Read and interact with product reviews according to authorization rules.

The result must look and behave like a coherent ecommerce application rather than a collection of disconnected demo pages.
