# Clerk x shadcn/ui

Simply copy and paste the provided CSS into your `globals.css` file, and voilà—your Clerk components will instantly match the shadcn/ui style!

```css
/* =========================================
   Clerk × shadcn 
   ========================================= */
@layer components {
  .cl-shadcn {
    /* Buttons */
    .cl-formButtonPrimary,
    .cl-profileSectionPrimaryButton,
    .cl-userButtonPopoverActionButton,
    .cl-accordionTriggerButton,
    .cl-navbarButton {
      @apply rounded-2xl bg-primary text-primary-foreground focus-visible:ring-ring ring-offset-background inline-flex h-9 items-center justify-center px-3 font-medium whitespace-nowrap shadow-none transition-colors focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:outline-none disabled:pointer-events-none disabled:opacity-50;
    }

    .cl-formButtonPrimary:hover {
      @apply bg-primary/90;
    }

    /* "Secondary-ish" button hover text only */
    .cl-userButtonPopoverActionButton,
    .cl-profileSectionPrimaryButton,
    .cl-accordionTriggerButton,
    .cl-navbarButton {
      @apply hover:text-accent-foreground;
    }

    /* Destructive (keep color tokens consistent) */
    button[data-localization-key="userProfile.start.dangerSection.deleteAccountButton"] {
      @apply bg-destructive text-destructive-foreground hover:bg-destructive/90;
    }

    /* Cards & surfaces */
    .cl-card,
    .cl-socialButtonsBlockButton,
    .cl-alert,
    .cl-phoneInputBox,
    .cl-userButtonPopoverCard,
    .cl-userButtonPopoverMain,
    .cl-menuList,
    .cl-actionCard {
      @apply bg-background border-input rounded-2xl border;
    }

    .cl-card,
    .cl-cardBox {
      @apply shadow-sm;
    }
    .cl-card {
      @apply shadow-md;
    } /* stronger on main card */

    /* Text colors */
    .cl-headerTitle,
    .cl-socialButtonsBlockButtonText,
    .cl-loading,
    .cl-formFieldLabel,
    .cl-formHeaderTitle,
    .cl-selectButton__countryCode,
    .cl-selectButton__countryCode p,
    .cl-selectOption p,
    .cl-selectOption div,
    .cl-modalCloseButton,
    .cl-navbarButton,
    .cl-breadcrumbsItem.cl-breadcrumbsItem__currentPage,
    .cl-profileSectionTitle p,
    .cl-userPreviewTextContainer,
    .cl-profileSectionContent p,
    .cl-form p,
    .cl-accordionTriggerButton,
    .cl-internal-icon,
    .cl-userPreviewSecondaryIdentifier__userButton,
    h1[data-localization-key="userProfile.navbar.title"],
    .cl-menuButton {
      @apply text-foreground;
    }

    .cl-headerSubtitle,
    .cl-dividerText,
    .cl-footerActionText,
    .cl-alertText,
    .cl-formFieldInfoText,
    .cl-formFieldSuccessText,
    .cl-identityPreviewText,
    .cl-userButtonPopoverActionButtonText,
    .cl-userButtonPopoverFooter p,
    .cl-userButtonPopoverFooter a,
    .cl-formHeaderSubtitle,
    .cl-breadcrumbsItem,
    .cl-breadcrumbsItemDivider,
    .cl-fileDropAreaHint,
    .cl-fileDropAreaFooterHint,
    .cl-form
      p[data-localization-key="userProfile.emailAddressPage.emailCode.formHint"],
    p[data-localization-key="userProfile.profilePage.successMessage"] {
      @apply text-muted-foreground;
    }

    .cl-userButtonPopoverFooter a {
      @apply hover:text-muted-foreground;
    }

    /* Links */
    .cl-footerActionLink {
      @apply text-accent-foreground hover:text-accent-foreground/90 underline;
    }
    .cl-formResendCodeLink {
      @apply text-primary disabled:opacity-90;
    }

    /* Inputs (text/email/password/search/etc.) */
    .cl-formFieldInput[type="text"],
    .cl-formFieldInput[type="email"],
    .cl-formFieldInput[type="password"],
    .cl-selectSearchInput__countryCode {
      @apply rounded-2xl border-input bg-background text-foreground placeholder:text-muted-foreground ring-offset-background focus-visible:ring-ring flex h-10 w-full border px-3 py-1 file:border-0 file:bg-transparent file:text-sm file:font-medium focus-visible:ring-2 focus-visible:ring-offset-2 focus-visible:outline-none disabled:cursor-not-allowed disabled:opacity-50;
    }

    .cl-otpCodeFieldInput {
      @apply border-input text-foreground border;
    }

    /* Select menu / options */
    .cl-selectOptionsContainer__countryCode {
      @apply border-input bg-background border;
    }

    /* Dividers & borders */
    .cl-dividerLine {
      @apply bg-border;
    }
    .cl-profilePage > .cl-header,
    .cl-profileSection__profile,
    .cl-profileSection__emailAddresses {
      @apply border-b;
    }

    /* Badges */
    .cl-badge {
      @apply rounded-2xl border-input bg-background text-foreground border px-2.5 py-2 text-xs shadow-none;
    }
    .cl-badge[data-localization-key="badge__unverified"] {
      @apply text-destructive border bg-transparent;
    }

    /* Footer / Navbar / Scroll containers (use gradients softly) */
    .cl-footer {
      @apply bg-background rounded-b-folli border-x border-b;
      background-image: none;
    }
    .cl-userButtonPopoverFooter {
      @apply rounded-b-folli bg-transparent;
    }
    .cl-navbar {
      @apply rounded-l-folli bg-background border-y border-l;
    }
    .cl-scrollBox {
      @apply rounded-2xl border-input bg-background rounded-l-none border;
    }
    .cl-navbarMobileMenuRow {
      @apply rounded-t-folli bg-background border-x border-t;
    }
    .cl-navbarMobileMenuButton {
      @apply text-foreground;
    }

    /* Social buttons */
    .cl-socialButtonsBlockButton,
    .cl-alternativeMethodsBlockButton {
      @apply h-10 shadow-none;
    }
    .cl-socialButtonsBlockButton {
      @apply border;
    }
    .cl-alternativeMethods .cl-alternativeMethodsBlockButton {
      @apply border-input text-muted-foreground h-10 border;
    }

    /* Menus */
    .cl-menuItem[data-color="neutral"] {
      @apply text-foreground hover:bg-muted;
    }
    .cl-menuButton {
      @apply hover:text-foreground;
    }

    /* File drop */
    .cl-fileDropAreaBox {
      @apply bg-muted;
    }
    .cl-fileDropAreaIconBox {
      @apply bg-muted/70;
    }
    .cl-fileDropAreaIcon {
      @apply text-muted-foreground;
    }
    .cl-fileDropAreaButtonPrimary {
      @apply text-foreground hover:bg-secondary hover:text-accent-foreground h-10 px-2.5 py-1 transition-colors;
    }

    /* Avatars */
    .cl-avatarImageActionsUpload {
      @apply border-input text-foreground border;
    }

    /* Sizes */
    .cl-internal-t38b9v {
      /* width container (stable enough but still optional) */
      @apply w-full md:min-w-[36rem] lg:w-[55rem];
    }

    /* Hide/clean up minor chrome (prefer stable public classes/roles where possible) */
    .cl-buttonArrowIcon {
      @apply hidden;
    }
  }
}
```
