# Portfolio refresh: plan and content evidence

Reviewed October 19, 2026. This is a static HTML/CSS enhancement; no framework,
runtime dependency, hosting configuration, or deployment workflow was added.

## Implementation steps

1. Refine the original palette and typography; create a compact two-column hero.
2. Use one shared project-card structure with a visual, summary, tags, technical
   accomplishments, and a case-study link or native details disclosure.
3. Replace generic focus areas with verified capabilities; add experience,
   the supplied resume, and professional contact actions.
4. Add the Veilkeeper architecture case study and verify markup, navigation,
   assets, keyboard interactions, and responsive layouts.

## Evidence used

- The original portfolio supplies the GitHub, LinkedIn, studio, and game URLs.
- The user explicitly designated john@johnserwatka.com as the intended personal
  business address in the final polish pass. Both portfolio contact actions and
  the visible address use it. The supplied resume already uses the same address.
- The newly supplied John_Serwatka_Resume.pdf is copied without modification to
  files/. The matching Word document verifies role names, employment dates,
  transferable school-operations responsibilities, Python/JavaScript experience,
  and support practices. The older IT Support resume additionally describes
  client troubleshooting and maintenance, and FreeScout issue follow-up.
- The user confirmed that Higgins Dash used Wix and that their main duties were
  gathering requirements from owners/managers, gathering site information, and
  getting layouts for it. The card emphasizes this rather than implying a custom
  application build. No unverified client URL or repository was added.
- Veilkeeper's current local development checkout at b490d4b provides
  Scripts/Controllers/ICombatController.cs, HumanController.cs, AIController.cs,
  ControllerInputBridge.cs, Tests/Smoke/SmokeHarness.cs, .github/workflows/ci.yml,
  and the ci-smoke recipe. Architecture and Testing Strategy notes corroborate
  the design, the 20-fight CI configuration, and test limitations. Twenty is a
  configured smoke batch, not a newly executed benchmark or balance result.
- The architecture comparison in the case study is an analysis of alternatives,
  not a claim that the owner prototyped each approach.
- The public Veilkeeper GitHub repository is an overview; it is not labeled as
  public source code. Public alpha downloads and PlayNYC feedback are documented
  at https://pocketlore-studios.itch.io/veilkeeper and its development log.
- The eight new Steam captures supplied on October 19, 2026 were reviewed through
  the Desktop symlink "Veilkeeper Steam Screenshots" (Veilkeeper app 4515130).
  Their visible version stamp is 0.1.2.0 alpha. They show the raised isometric
  board, floating crystal cursor, movement paths, and current input hints.
- The hero uses 20261019111438_1.jpg, copied without modification to
  img/veilkeeper-isometric.jpg. The attack preview shows projected damage, health
  after the exchange, and counterattack information, supporting the combat
  architecture case study.
- The project card uses 20261019111424_1.jpg, copied without modification to
  img/veilkeeper-movement.jpg. It shows the Assassin's movement range and routed
  path to the crystal cursor. Both original images are 1920×1080 JPEGs.
- The caption identifies the captured build and capture date; it does not claim
  final artwork or that a particular store download has been updated. The user
  confirmed public downloads are only on itch.io; Steam builds require internal
  tester access. The hero and case study now state this explicitly. The earlier
  September Steam captures and October game-site image were superseded for this
  portfolio selection. The Steam originals and game-site assets are retained.
- The homelab README and operating runbook verify Beelink hardware, native
  NixOS services, Tailscale, Caddy, monitoring, backup preparation, and recovery
  workflows. Docker is earlier experience from the resume/original portfolio;
  it is not presented as the current server's service runtime. No internal
  addresses, hostnames, credentials, or private service URLs were copied.
- Veilkeeper's accepted ADR 0009 and tools/release-archive source/tests verify
  the Rust archive path: clean-worktree exports, embedded provenance readback,
  checksummed manifests, deterministic packages, no-overwrite archive promotion,
  pre-push verification, preflight checks, and failure/retry handling. The VK-37
  store-upload plan and current module/test implementation show ongoing work;
  the portfolio does not claim a finished, validated store-publishing pipeline.

## Maintenance notes

- Replace files/John_Serwatka_Resume.pdf when a newer public resume is ready.
- Keep release-tool status in sync with implementation and validation evidence.
- Keep the image and caption in sync with the game's published development view.
- Keep practical experience distinct from additional language familiarity.
- No package manifest, formatter/lint configuration, type checker, or build
  command existed in this repository. Its HTML/CSS is served directly.

## Verification results

- Prettier parsed and formatted the changed HTML, CSS, and Markdown; its final
  check passed. Used the already installed formatter from the neighboring game
  website checkout, without adding a dependency or package manifest here.
- All five HTML pages passed checks for balanced elements, one primary heading,
  unique IDs, image descriptions/dimensions, local destinations, and fragment
  references. The existing information, privacy, and 404 pages were included.
- Chromium checked the homepage, case study, rclone information page, and rclone
  privacy page at 320, 390, 640, 760, 768, 820, 1024, and 1440 pixels: 32 layouts,
  with no horizontal overflow, broken images, or browser runtime errors.
- The skip link was the first keyboard stop. The project disclosure opened with
  Enter, a visible focus outline was present, and reduced-motion preferences
  disabled smooth scrolling.
- The homepage, case study, and resume returned HTTP 200 from the local preview;
  the resume was served as application/pdf and matches the supplied PDF exactly.
- git diff --check passed. There are no existing lint, type-check, or build
  commands to run. No deployment was performed.

The factual gaps raised during implementation were resolved by the supplied
resume and the user's Higgins Dash clarification. A final owner review of the
case-study narrative and experience wording remains an editorial recommendation.
