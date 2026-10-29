# Cat Velvet — local navigable draft

First version: 2026-10-28, Central Time. Provisional identifier selected by the user: `catvelvet`. This is a local Zoolanding draft, not a published domain or a registered remote draft repository.

## Preview

Run the hub development server, for example `npm start -- --host 127.0.0.1 --port 4300`, and open:

- Home: `http://127.0.0.1:4300/?draftDomain=catvelvet&debugWorkspace=false`
- Shipping form: `http://127.0.0.1:4300/pedido?draftDomain=catvelvet&debugWorkspace=false`
- Privacy draft: `http://127.0.0.1:4300/privacidad?draftDomain=catvelvet&debugWorkspace=false`

All three routes use the shared Zoolanding renderer and native JSON components. Shared navigation and footer live in root `components.json`; each route owns its page payload. The shipping route uses the native embed-frame component for the official Google Forms iframe. No custom HTML, scripts or stylesheets are used. The shared renderer mounts the iframe immediately while keeping native lazy loading, avoiding a skipped viewport-placeholder trigger during fast scrolling. Appearance is authored with Angora utilities and the local theme.

The approved design uses warm white, peach, blush and plum text. The hero reuses the gallery's clean upper-angle image on blush, with its natural square proportions and the existing rounded frame on the peach section. The product gallery contains three AI-edited listing references with clean blush, warm-white and peach backgrounds. All images are identified as illustrative references and served from local draft assets. See [asset provenance](assets/README.md) for sources and publication follow-up.

## Functional scope

- Section navigation, mobile menu, visible question-and-answer content, legal-status accordions and links between home and `/pedido`.
- Three-view product gallery (upper angle, side angle and illustrative scale), using native interaction-scope state and accessible thumbnail buttons. Selection changes the main image, caption, border and accessible button label without navigation or external requests.
- Technical facts reached by “Conocer mi producto”: brand, design, color, silicone, ten suction settings, single-button/app control, sound level and water resistance with IP grade pending. Copy uses direct labels without repeated “según el anuncio” phrasing. [Source notes](product-specs.md) retain provenance and unresolved details. Measurements, actual weight, charging, battery life, app compatibility, IP/immersion and manufacturer care instructions remain unverified. The scale image does not establish measurements; its lipstick prop is not included.
- A published Google Form embedded at `/pedido` collects nine shipping fields: seven required, with interior and references optional. Postal validation requires five digits. Responses save into a linked private Google Sheet in the existing project Drive folder; the sheet/editor URL is not present in public payloads. See [shipping handoff](checkout.md).
- The form has a rose accent inside the peach landing frame, with a direct respondent-link fallback. Email collection, one-response/login restriction and public response summaries are off. One clearly marked fictitious integration response remains; it is not a purchase.
- All nine questions have visible filling examples and short instructions. Google Forms retains its fixed short-answer placeholder; the supported question descriptions provide persistent guidance. Current account ownership is temporary; the doctor's account is the intended future owner of both Form and Sheet, with the destination/handoff still pending.
- The WhatsApp destination is intentionally omitted. A disabled button and pending-number notice are shown. A conditional native link is prepared for later activation, using a generic message rather than shipping details in its URL. Matching the form response uses the same name/telephone in the chat.
- No payment gateway, backend order record, real order number, inventory reservation or Calendly destination is configured. Google stores shipping responses only. Availability, product/shipping total, payment instructions and receipt validation are handled in the future WhatsApp conversation. The receipt is attached in WhatsApp, not uploaded to Forms.
- The `#agenda` section explains manual post-payment scheduling: validated payment → invitation through WhatsApp → choose a time in Calendly → complete the reservation. The Calendly button stays disabled with a pending-link notice. The shipping page explains the same manual sequence without marking payment validated or a session booked.
- Use fictitious values during review: submitting the embedded form saves to Google. Runtime analytics are disabled. Landing preview pages are marked `noindex,nofollow`.
- The professional presentation now uses the name, master's title, clinical psychology/sexology profile, degree credential and four specialization areas supplied by the user. The included session retains its educational scope. A portrait has not been supplied; no stock or generated portrait is used.
- Nationwide Mexico shipping is confirmed by the user; the charge depends on destination and is quoted before payment. Carrier selection and delivery estimates remain pending. The customer flow does not require identifying who prepares packages.
- The shared footer and shipping page link to a complete-layout privacy draft at `/privacidad`, naming the user-confirmed individual controller. The address and monitored privacy contact email remain missing. [Reusable Spanish privacy text](privacidad-borrador.md) includes a short Google Forms notice for later completion; it has not been installed in the public Form. See [checkout privacy handoff](checkout.md#privacy-draft).
- Price, commercial contact, carrier/timing, product manual, completed privacy notice, warranty/returns and session conditions remain pending. Focused source research did not resolve exact package contents, charging, measurements, runtime, official app compatibility or care; no generic rose-device specifications were adopted.
- Search and answer-discovery preparation includes descriptive product/session headings, nine visible answers, route-specific Spanish metadata, product social imagery and related business/product/service structured data. Initial server HTML includes the content. No price, reviews or professional identity were fabricated. See [SEO and AEO handoff](seo-aeo.md) for verified scope, current search guidance and publication prerequisites.

## Next production decisions

Confirm canonical domain and approved aliases before creating a remote draft repository or registering it in the fleet. The provisional name is sufficient for local preview but is not accepted by every domain-based publishing/readiness tool. Keep existing `dev -> test -> main` promotion and upload-grant workflows for any later publication. Do not infer that the local asset is available in a shared environment.

Task-local evidence and scripts remain in the hub's ignored process/evidence surfaces. No commits or uploads were made for this local version.
