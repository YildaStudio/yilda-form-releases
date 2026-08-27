=== Yilda Form ===
Contributors: yildastudio
Tags: form, giveaway, landing page, participant data, vmix
Requires at least: 5.8
Tested up to: 7.0
Requires PHP: 7.4
Stable tag: 1.0.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Create on-brand forms for giveaways and campaigns, with their own landing page, banners, and exports ready for Yilda Draw.

== Description ==

Yilda Form is the data-capture companion to **Yilda Draw**. Create custom forms for your campaigns or promotions, capture your participants' data with their own on-brand landing page, and export the entries ready for the draw — without writing a single line of code.

= Up to 7 forms at once =

Each form ("design") automatically generates and publishes its own page as soon as you save it — no need to create the page separately or pick a template by hand. You can have up to 7 forms active at the same time, each with its own appearance, fields, and page. Each one can be paused, duplicated, or deleted independently, and a sample form with Yilda Studio's brand palette is created on install so you're not starting from scratch.

= A form customized for every campaign =

* Configurable capture fields: full name, city, country, contact, and ID number, with the option to reorder them by dragging.
* Optional custom question, to ask for any extra piece of information your campaign needs (a single open-text question per form).
* Optional consent checkbox, with editable text, required to submit the form if enabled.
* Colors, button, header, and footer images configurable per form — each design has its own palette, fully independent from the others.
* Independent on-brand banners for desktop (vertical, 300×900px) and mobile (horizontal, 800×200px), each with an optional link.
* Customizable thank-you message after a successful entry.

= Entries and export =

* Entries screen with a per-form summary (entry count and date of the latest one), plus a filterable, paginated detail view per form.
* Export to Excel on an on-brand template — the only format Yilda Draw reads directly.
* Export to CSV as a secondary backup (Yilda Draw does not read it directly).
* Both exports process entries in batches (cursor-based), built for large numbers of participants with no duplicates or gaps.
* Entries can be cleared for a single form, for the ones with "no page assigned," or for all forms at once, always with explicit confirmation showing the exact count before deleting.

= Security and privacy =

* Configurable limit on entries per IP within 24 hours (5-10 recommended), with a manually blocked IP list and a recent-activity-per-IP screen.
* Real IP detection by default — it never trusts headers a visitor could fake — with optional, explicit support for sites behind a trusted proxy or CDN (Cloudflare, Nginx, etc.), choosing a single header manually instead of trying several.
* The IP log used for the limit clears itself every 24-48 hours via a scheduled task.
* Validates that every submission belongs to a real, published page with a design assigned by the plugin — it does not accept entries with tampered page data.
* Data is kept if the plugin is deleted, unless explicitly set otherwise in Security (checkbox enabled by default).
* No formula injection in CSV exports.
* Optional consent checkbox text accepts a link (e.g. to your site's privacy policy).
* Suggests the personal data it collects to WordPress' own Privacy Policy Guide (Settings → Privacy), ready to paste into your site's privacy policy.

= QR codes =

Each form has its own QR code (linking directly to its URL), downloadable as a PNG from the Dashboard or from the page editor — generated with a library bundled in the plugin, with no dependency on any external service.

= Available in 6 languages =

The plugin is fully translated: Spanish (original language), English, Brazilian Portuguese, German, Japanese, and Indonesian. WordPress automatically shows the language configured for your site.

== Installation ==

1. Upload the `yilda-form` folder to `/wp-content/plugins/`, or install the .zip from Plugins → Add New → Upload Plugin.
2. Activate the plugin from the Plugins menu. On a fresh install, a sample form is automatically created with Yilda Studio's brand palette.
3. Go to **Yilda Form → Designs → + New design**, set up the content, fields, and appearance, and click **Save design**. Its page is created and published automatically.
4. On that same screen you'll see the form's URL and its QR code, ready to use.
5. Repeat step 3 for each additional form you want active at the same time (up to 7).
6. Submissions appear in **Yilda Form → Entries**, grouped by form, exportable to Excel or CSV.
7. Optional: check **Yilda Form → Security** to adjust the per-IP entry limit, and **Documentation** for the full guide with FAQs.

== Frequently Asked Questions ==

= Do I need Yilda Draw to use this plugin? =

No. The plugin works independently to create forms and capture participants. Yilda Draw is Yilda Studio's giveaway app, which can read the Excel file this plugin exports directly.

= How many forms can I have active at once? =

Up to 7. Once you hit the limit, you need to delete or duplicate an existing one to create another. Deleting a form does not delete the entries it already received.

= What happens to my data if I delete the plugin? =

By default, nothing — your forms and participants stay intact in the database. This is controlled by the "Keep the data if the plugin is deleted" option in Security, enabled by default.

= Does the plugin work behind Cloudflare or another proxy? =

Yes. By default it identifies each visitor by their real connection; if your site uses a proxy or CDN, you can configure it explicitly in Security, choosing a single trusted header, so it correctly and safely recognizes each visitor's real IP.

= Can I use the CSV to load data into Yilda Draw? =

Not directly — Yilda Draw only reads the Excel file with the official template. The CSV is a secondary backup; if you use it, you'll need to paste the data into the Excel template by hand before loading it into the app.

= What languages is it available in? =

Spanish (the plugin's original language), English, Brazilian Portuguese, German, Japanese, and Indonesian. It's applied automatically based on your WordPress site's configured language.

= Can I have different fields on each form? =

Yes — each design has its own field, order, color, banner, and text configuration, fully independent from any other active forms you have.

= Does the plugin add its own privacy policy or terms and conditions? =

No — those depend on your giveaway's own rules and your legal identity as the organizer, so the plugin can't write them for you. What it does do is tell WordPress which personal data it collects (name, city, contact, country, ID number, the custom question, and the IP for 24-48 hours): that text shows up ready to copy under **Settings → Privacy → Policy Guide**, for you to add to your site's privacy policy. The consent checkbox text also accepts a link, so you can point it directly at your policy.

== Screenshots ==

1. Dashboard with a summary of forms and recent entries.
2. Design editor, with a live preview.
3. Public landing page of a form, with brand banners.
4. Entries screen, with the per-form summary.

== Changelog ==

= 1.0.0 =
* First public release.
* Multiple-form system (up to 7 active), each with its own page, fields, appearance, and banners.
* Export to Excel (format read by Yilda Draw) and CSV, in batches.
* Security: per-IP entry limit, manual blocking, configurable trusted-proxy IP detection.
* Optional consent checkbox and custom question field.
* QR code per form.
* Available in 6 languages: Spanish, English, Brazilian Portuguese, German, Japanese, and Indonesian.

== Upgrade Notice ==

= 1.0.0 =
First public release.
