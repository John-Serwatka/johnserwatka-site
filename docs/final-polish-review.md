# Final portfolio polish review

Reviewed October 19, 2026. The approved layout, theme, hero composition, and
project structure were preserved. No framework, dependency, or deployment
configuration was changed.

## Changes and verification

| Area                       | Result                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Resume                     | John_Serwatka_Resume.pdf exists, opens in Poppler, and renders as one readable US Letter page. Descriptive filename retained. HTTP 200 and application/pdf locally. Byte-identical to the supplied PDF; no resume changes.                                                                                                                                                   |
| Contact                    | Both mailto actions and the displayed address now use john@johnserwatka.com, explicitly requested by the owner. The resume already uses this address.                                                                                                                                                                                                                        |
| Build availability         | Screenshot caption identifies development build v0.1.2.0 and capture date. The owner confirmed the public alpha is only on itch.io; Steam builds require internal tester access. Hero and case study state this explicitly.                                                                                                                                                  |
| Release engineering        | Implemented archive verification is supported by accepted ADR 0009, the Rust implementation, and verification/retry/failure tests in the Veilkeeper checkout at b490d4b. Store-upload work has supporting modules and a test harness, but end-to-end publishing validation remains incomplete; copy retains that distinction. No release commands or store uploads were run. |
| Project cards              | Shortened introductory copy without dropping technical accomplishments. Added a minimum visual height to prevent diagram text clipping at tablet widths. Cards keep their own height when a neighbor's details expand.                                                                                                                                                       |
| Sticky navigation          | All 36 tested anchor destinations across the three widths kept their headings below the header. Existing scroll offsets needed no change.                                                                                                                                                                                                                                    |
| Responsive layouts         | Homepage, case study, and both existing rclone pages passed at 390, 768, and 1440 pixels: 12 page/viewport combinations, without horizontal overflow or broken images.                                                                                                                                                                                                       |
| Keyboard and accessibility | Six keyboard runs covered 137 control focus stops. Skip links, visible focus, native disclosures, and reduced-motion behavior passed. Accessibility-tree checks found no unnamed links or controls. Figure caption placement was corrected.                                                                                                                                  |
| Contrast and imagery       | Checked DOM text against its computed background on both portfolio pages; minimum sampled ratio was 7.74:1. Secondary button borders were strengthened. Gameplay image alt text describes the actual development-build captures. Text embedded inside screenshots is not covered by the DOM contrast check.                                                                  |
| SEO and sharing            | Distinct titles/descriptions retained. Added canonical URLs, author metadata, Open Graph and large-image Twitter card metadata, absolute image URLs, image dimensions, and descriptive image alternatives on both pages. Existing real gameplay imagery is used. Metadata and local image responses passed; production preview cards require deployment.                     |
| Static checks              | All five HTML files passed balanced markup, heading, unique-ID, local-destination, and fragment checks. Prettier and git diff --check passed. No existing build, lint, or type-check commands are configured in this static repository.                                                                                                                                      |

Resume SHA-256 (unchanged):
`694f93170752046df55a3e4f6b19bf6e7beee5d9d62f640050e3ede941620aa2`.

## Public link checks

HTTP 200 was returned by the personal GitHub profile, the Veilkeeper public
project overview, itch.io alpha page, PlayNYC feedback update, PocketLore Studios,
Veilkeeper game site, and Steam listing. The public GitHub project is still
correctly labeled as an overview rather than public game source.

LinkedIn returned HTTP 999 to the automated client. The original profile URL was
preserved and is corroborated by the supplied resume and GitHub profile, but
opening it in an ordinary signed-in browser remains a manual check.

The johnserwatka.com domain publishes Cloudflare mail-routing MX records. This
confirms domain-level routing, not successful delivery to the specific mailbox.
No test email was sent, and no mail configuration was changed.

## Publication concerns

The live homepage returns HTTP 200 but is still the older portfolio. These new
destinations currently return HTTP 404 publicly, while passing in the local
preview:

- /files/John_Serwatka_Resume.pdf
- /projects/veilkeeper/
- /img/veilkeeper-isometric.jpg (also the social preview image)

The updated portfolio, resume, case study, and preview image must be included in
the normal deployment before they can be verified on the public domain. This
review did not deploy or change hosting.

## Final targeted validation addendum

The approved homepage organization and case-study narrative were retained. This
pass made only the requested header, diagram, and supporting-evidence changes:

- Replaced the header's translucent fill with the solid shared background color.
  Its existing sticky positioning and z-index are retained with explicit stacking
  isolation. Scrolled browser checks confirmed an opaque rgb(15, 17, 21) fill,
  opacity 1, top position 0, and the header above page content at all three widths.
- The architecture diagram now has two controller boxes with visible branches
  merging into shared combat execution, followed by CombatManager. Native HTML,
  CSS, and a small inline SVG provide the visual. Its accessible graphic name and
  description explain both input sources, their convergence, validation and
  sequencing, and board mutation. Browser accessibility-tree checks verified both
  name and description; normal scrolled views were inspected at all three widths.
- Added a brief Engineering outcome summary near the beginning, covering shared
  validation, real-scene full-match testing, and the input-bridge and asynchronous
  sequencing trade-offs. No existing case-study sections were rewritten.
- Added two authentic summary messages from the saved local CI smoke log dated
  October 12, 2026. They record 20 fights, zero timeouts, zero invalid outcomes,
  zero bootstrap errors, and the pass sentinel. An exact comparison verified that
  only the logging prefixes were removed. The example contains no paths,
  credentials, URLs, internal addresses, or private repository identity. It is
  explicitly labeled as a local run of the CI check, not a hosted CI result or a
  balance benchmark. The full log was not copied into the portfolio.

The CI workflow, its shared recipes, and the smoke harness were rechecked: the
workflow invokes the same smoke recipe, its configured batch is 20, gdUnit4 tests
run separately, and smoke failures propagate through the pass/fail sentinel and
exit status. This pass did not trigger game builds, a new game CI run, or store
uploads. Development/public availability remains correctly labeled: the captured
v0.1.2.0 build is a development build, public alpha downloads are on itch.io, and
Steam builds require internal tester access.

Final website checks passed: 12 page/viewport combinations at 390, 768, and 1440
pixels, 36 anchor checks, six keyboard-navigation runs, visible focus, disclosures,
reduced motion, contrast, image loading, accessible names, diagram branch layout,
all five HTML pages' markup/SVG/IDs/local references, Prettier, and git diff
--check. No build or type-check commands exist in this static repository.

The resume still opens and renders as the same one-page PDF and retains the hash
above. Both contact actions use john@johnserwatka.com. Public link checks returned
the same results and publication concerns recorded above: working external
project/profile destinations except LinkedIn's automated-client block, and new
portfolio destinations still pending deployment. Domain mail routing is present;
mailbox delivery was not tested. No additional infrastructure, dependencies, or
features were introduced. Work stops after this validation pass.
