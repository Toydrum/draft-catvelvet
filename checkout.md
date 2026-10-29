# Cat Velvet shipping and manual purchase handoff

Updated 2026-10-28 CT. The landing is a published noindex review on the shared test host; see [preview links](README.md#preview). Production remains disabled. The embedded Google Form is published and saves real responses; use fictitious data when reviewing.

## Simple operation

1. The customer enters shipping details in the Google Form embedded at `/pedido` and presses its Enviar button. A direct public-form link is available if embedding fails.
2. Google Forms stores the response in its linked private Sheet. Only the owning account has response-sheet access. Both files are in the existing cat velvet Drive folder. Do not expose the Sheet or editor URL in public payloads.
3. The customer uses the same name and telephone in WhatsApp so the owner can match the response. The owner confirms availability, product price, shipping cost and total, then shares payment instructions. The receipt is sent in that conversation.
4. The owner independently validates payment, coordinates shipping and shares the Calendly invitation. Shipping submission does not confirm a purchase, payment or session.

No order dashboard, folio, payment gateway, duplicate native form, form-to-WhatsApp data transfer or automatic booking is configured. The landing does not read the cross-origin submission state or claim an automatic transition after submission.

## Form configuration

Public respondent form: [Cat Velvet · Datos de envío](https://docs.google.com/forms/d/e/1FAIpQLSez96L6aCqtY01JCHl9TIe1DBmz2LSrEQRrvXSA_i4MXkUYbQ/viewform).

- Seven required short-text fields: recipient name, contact telephone, street/exterior number, neighborhood, municipality, state and postal code.
- Two optional short-text fields: interior number and delivery references.
- Mexico delivery scope appears in the description. No email, medical/session information, payment details, attachments or receipt is requested.
- Postal validation requires exactly five digits and preserves leading zeros.
- Each of the nine questions includes a persistent description with an illustrative example and a short filling instruction. Examples distinguish street/exterior from interior, neighborhood from municipality, and postal leading zeros. The form introduction tells respondents to replace examples with their own data. Google Forms controls the fixed short-answer placeholder; examples use its supported question-description field rather than prefilled answers.
- Email collection, one-response/login restriction and respondents' result summary are off. A signed-in visitor may still see their own Google account controls supplied by Google.
- Confirmation explains that shipping details were saved and that payment and session confirmation happen separately. The repeat-response link is off.
- Theme uses the brand rose accent; the landing's peach frame and warm-white surroundings complete the palette. Google controls the embedded form's internal appearance.

One explicitly marked integration-test response remains in Forms and the linked Sheet. It contains only fictitious values and must not be fulfilled.

## Future ownership

The user confirmed that the current account is temporary and the doctor's account will own the setup later. No destination account has been supplied and no access or ownership changes are authorized for this step. When the destination is available, verify the permitted ownership handoff for both the Form and linked Sheet, preserve private responses, and retest the published respondent link and landing embed. Moving a Drive folder alone is not an ownership change. Keep the current owner and public form link intact until that handoff is confirmed.

## Pending destinations

Commercial WhatsApp is intentionally absent from `variables.json`; continuation stays disabled until the owner supplies the number. Once supplied, set `variables.ui.contact.whatsappPhone` in international format and update pending copy. The native conditional link uses `whatsAppUrl` to prepare a generic conversation, without copying addresses into URL parameters. The customer chooses when to send it.

Calendly URL, session duration, availability and rescheduling/cancellation conditions remain pending. The owner shares the actual agenda privately after payment validation; no public booking destination is enabled.

The user confirmed nationwide Mexico shipping. The charge varies by destination and must be quoted, together with the product total, before payment. Carrier selection and delivery estimates still need confirmation. No flat rate, free-shipping promise or guaranteed delivery time is configured; package-preparer identity is not needed in customer copy.

Price, product manual, completed privacy notice, guarantee and return terms remain launch dependencies. Warranty is unknown; do not invent durations, exclusions or a no-warranty/no-return policy.

## Privacy draft

The local `/privacidad` route and [Spanish reusable copy](privacidad-borrador.md) name the user-confirmed individual controller, describe shipping, private Forms/Sheets storage, separate WhatsApp/payment handling, minimal carrier data and future scheduling, and provide a draft ARCO/revocation procedure. A short notice appears before the embedded form and links to the full local draft. The controller's address and privacy contact email remain explicit placeholders. A privacy contact is simply a monitored address for data requests and may be the business support email.

The short Google Forms notice is prepared in the same document but has not replaced the public form's description: it still lacks the controller's address, contact and a public full-notice URL. Do not insert a localhost link into the public Form or treat the incomplete draft as the final notice. Complete these details, confirm the actual provider/retention arrangements and any consent needed for intimate or financial information, then place the completed short notice before the Google Forms fields, including for direct-link visitors. Professional-session information needs separate handling if sensitive information is requested. Current technical ownership and the future account handoff remain as described above.

## Verification and maintenance

Check desktop/mobile home, `/pedido` and `/privacidad` after copy, theme or embed changes. Verify seven required/two optional fields, postal validation, confirmation, private Sheet receipt, no public result summary and pending commercial destinations. The shared native embed component keeps its existing sandbox policy; no custom HTML/script or relaxed iframe policy is needed. It mounts immediately and uses native iframe lazy loading, so fast scrolling cannot skip an empty wrapper viewport trigger and leave the form absent.
