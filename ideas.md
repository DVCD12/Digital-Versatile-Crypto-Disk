# DiscWallet — Design Brainstorm

## Three Stylistic Approaches

### 1. Y2K Optical Deck
**Intro:** Late-90s/early-2000s hi-fi CD deck aesthetic — brushed dark metal, VFD-green segment displays, chunky physical buttons. The wallet feels like a piece of stereo hardware.
**Probability:** 0.07

### 2. Cyber-Vault Neon
**Intro:** Neon-cyberpunk vault with glowing magenta/cyan edges and glitch effects. High drama, high saturation.
**Probability:** 0.03

### 3. Clean Lab Minimal
**Intro:** Sterile white laboratory look with soft shadows and clinical typography, framing the disc as a scientific specimen.
**Probability:** 0.02

---

## CHOSEN: Y2K Optical Deck

**Design Movement:** Late-1990s Japanese hi-fi hardware design (Sony ES / Denon / Pioneer CD decks) crossed with modern dark-UI craft. Skeuomorphic restraint: real-feeling hardware cues without kitsch.

**Core Principles:**
1. **Hardware honesty** — the app IS a device. Panels have machined edges, screws, vents, status LEDs. Every state change is a mechanical event.
2. **Instrument legibility** — data is displayed like a front-panel readout: monospace, high-contrast, amber/green phosphor glow.
3. **One moving part** — the disc is the hero. It spins, wobbles light, and dominates the idle screen; everything else is static chassis.
4. **Deterministic calm** — no random decoration. Every element maps to a function (LED = drive activity, readout = wallet data).

**Color Philosophy:** Near-black charcoal chassis (oklch ~0.16) evokes anodized aluminum at night. The single signature color is **phosphor amber (#FFB000-ish, oklch 0.8 0.16 75)** — the color of vintage drive-activity LEDs and VFD displays — used for the activity LED, live balance digits, and primary CTA. A secondary cool green for "locked/ready" states. Iridescent rainbow is reserved exclusively for the CD surface itself, making the disc the only polychrome object on screen.

**Layout Paradigm:** A centered vertical "rack unit" — the app is one 19-inch rack faceplate floating on a dark textured backdrop. Inside the faceplate, asymmetric split: disc/tray visualization on the left ~55%, readout panel on the right ~45% (stacks on mobile). Header is a thin machined strip with model number ("DW-1000") and brand mark. No scrolling marketing sections — it's a device, not a landing page.

**Signature Elements:**
1. The **iridescent CD** rendered in CSS conic-gradients, spinning with real physics feel (slow idle wobble, fast blur while reading).
2. **Activity LED** — a small amber dot that blinks during reads and polling, solid when a wallet is loaded.
3. **VFD readout panel** — dotted/scanline texture behind amber monospace text for address, balance, fingerprint.

**Interaction Philosophy:** Interactions feel electromechanical. Buttons depress (scale + inset shadow), the tray "loads" with a slide animation, eject snaps the UI back with a quick mechanical retract. Feedback is instant; no decorative delays on user-initiated actions.

**Animation:** Disc idle spin 8s linear infinite with subtle hue rotation; reading state 0.6s spin with motion blur illusion. Screen transitions: tray slide 280ms cubic-bezier(0.23,1,0.32,1). LED blink 120ms steps. Button press 120ms scale(0.97). Respect prefers-reduced-motion (static disc, no blink).

**Typography System:** **"Chakra Petch"** (Google Fonts) for display/labels — its squared techno forms read as machined engraving. **"JetBrains Mono"** for all data readouts (addresses, hashes, balances). Hierarchy: engraved uppercase micro-labels (11px, letter-spacing 0.15em, muted) above large mono values.

**Brand Essence:** DiscWallet — the Solana wallet that lives on a disc; for crypto tinkerers who love physical media; different because your seed is the disc itself. Adjectives: mechanical, deterministic, nostalgic.

**Brand Voice:** Terse hardware-manual English. Examples: "INSERT DISC TO CONTINUE." / "TRAY LOCKED — WALLET DERIVED FROM MEDIA FINGERPRINT."

**Wordmark & Logo:** "DISCWALLET" set in Chakra Petch semibold with a thin ring glyph (stylized disc with center hub hole) as the mark; model designation "DW-1000" beside it like a product SKU.

**Signature Brand Color:** Phosphor amber (oklch 0.8 0.16 75) — the drive-activity LED color.
