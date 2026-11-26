\# Prompt: Nova Agent, light 3D robot landing page



Build a single-file \*\*three-section landing page\*\* for a fictional on-chain AI agent product, \*\*NOVA AGENT\*\* ("Thinking Machines"). Use plain HTML, CSS and vanilla JS, plus \*\*three.js 0.160.0\*\* as an ES module through an import map. There is no framework and no build step.



The page is warm paper-white with thin dark grid lines. A cute boxy white-ceramic robot is built entirely in three.js and stays fixed on a full-screen canvas behind the content:

\- \*\*Intro:\*\* the robot stands on a charcoal pedestal with its head tilted.

\- \*\*Product:\*\* the camera glides in to a close-up of the head.

\- \*\*Reviews:\*\* the face screen swaps its two glowing eyes for a quote mark.



\## Assets (all external URLs used)



\- \*\*three.js core:\*\* https://unpkg.com/three@0.160.0/build/three.module.js

\- \*\*three.js addons\*\* (import map prefix `three/addons/` → https://unpkg.com/three@0.160.0/examples/jsm/):

&#x20; - RoundedBoxGeometry: https://unpkg.com/three@0.160.0/examples/jsm/geometries/RoundedBoxGeometry.js

&#x20; - RoomEnvironment: https://unpkg.com/three@0.160.0/examples/jsm/environments/RoomEnvironment.js

\- \*\*Fonts\*\* (latin woff2; embed them as base64 `@font-face` in the single file):

&#x20; - IBM Plex Mono 300: https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3oQIwlBFgsAXHNk.woff2

&#x20; - IBM Plex Mono 400: https://fonts.gstatic.com/s/ibmplexmono/v20/-F63fjptAgt5VM-kVkqdyU8n1i8q131nj-o.woff2

&#x20; - IBM Plex Mono 500: https://fonts.gstatic.com/s/ibmplexmono/v20/-F6qfjptAgt5VM-kVkqdyU8n3twJwlBFgsAXHNk.woff2

&#x20; - Schibsted Grotesk 400/500 (variable): https://fonts.gstatic.com/s/schibstedgrotesk/v7/Jqz55SSPQuCQF3t8uOwiUL-taUTtap9GayojdSFO.woff2



There are no images or videos. The robot, the gradient ring texture and the face screen are all generated in code. The only other image is the small testimonial avatar, an inline SVG (a figure in front of a brick wall).



\## Palette and type



| Token | Value |

|---|---|

| Background | `#efece6` |

| Text | `#141414` |

| Dim text | `rgba(20,20,20,.5)` |

| Grid lines | `rgba(20,20,20,.09)` |

| Brand gradient | `conic-gradient(from 200deg, #ffb347, #ff8a3d 18%, #ff5a5f 34%, #ff3d8b 50%, #ff5a5f 66%, #ff8a3d 82%, #ffb347)` |



\- \*\*Sans:\*\* Schibsted Grotesk.

\- \*\*Mono:\*\* IBM Plex Mono, uppercase, letter-spacing .04–.06em, used for all small labels.



\## Fixed chrome



\- \*\*Grid:\*\* three 1px vertical guides at 17 %, 50 % and 83 % of the width (`--col: 17%`).

\- \*\*Top bar:\*\* 30px tall, mono 11px.

&#x20; - Text: "\*\*New:\*\* Nova Agent V1 Is Here - The Home for On-chain AI Agents ↗", with a × at the right.

&#x20; - It slides up out of view (0.5s, `cubic-bezier(.6,0,.2,1)`) once the page scrolls past 40px, or when × is clicked.

\- \*\*Nav:\*\* 52px tall, below the top bar (moves to top 0 when scrolled). Paper at 86 % with an 8px backdrop blur and a bottom hairline. Its grid columns are `17% 1fr 12% 17%`:

&#x20; - \*\*Logo:\*\* a 27px rounded-square outline (a C-shape) stroked with the orange→pink gradient, with two dark dots for eyes, then "NOVA AGENT" at 18px.

&#x20; - \*\*Menu (mono 11px):\*\* Solutions▾, Pricing, Learn▾, $NOVA▾, Community▾, Contact us.

&#x20; - \*\*Pad cell:\*\* "Nova Pad ↗", with hairlines on both sides.

&#x20; - \*\*Button:\*\* "•• LAUNCH NOVA", a 30px outlined mono button. A gradient border shows only along part of its top edge and down its left edge, cut with a clip-path.

\- \*\*Right rail:\*\* fixed, vertically centred, 270px tall.

&#x20; - A column of 14 tiny dots.

&#x20; - A floating label with a small dial icon, reading INTRO, PRODUCT or REVIEWS. It slides to 0 %, 31 % or 62 % of the rail as each section becomes more than half visible (0.7s).

&#x20; - "≡ MENU" underneath.



\## Section 1: Intro (100vh)



\- \*\*Prompt box:\*\* left edge at 17 %, top 30 %, width 24.4 %.

&#x20; - A 42px square tab containing a bold serif “.

&#x20; - Below it a 1px outlined box (mono 11px uppercase, line height 1.45) with an auto-typing prompt and a blinking 6×11px block caret.

&#x20; - Small 7px rounded corner brackets sit just outside the box.

&#x20; - Under the box, the next prompt shows in faint ink.

&#x20; - \*\*Typing:\*\* 38ms per character. It holds 2.6s, deletes 2 characters per 14ms, waits 250ms, then types the next prompt. The prompts loop:

&#x20;   1. "Create a smart contract for a token named NOVA on Ethereum."

&#x20;   2. "Explain what a smart contract does in simple terms."

&#x20;   3. "Audit this contract for reentrancy vulnerabilities."

&#x20;   4. "What is the market sentiment on BTC today?"

\- \*\*Rule:\*\* a hairline from the prompt box to the right guide, level with the top of the box.

\- \*\*Feature list:\*\* under that rule, right-aligned to the 83 % guide, 23 % wide. Rows are 21px tall with hairline dividers and a dot at 18 % of each row:

&#x20; - DEVELOPMENT

&#x20; - MARKET ANALYSIS

&#x20; - AI TRADING

&#x20; - AND MUCH MORE (dim)

\- \*\*Bottom left:\*\* "UNLEASH THE POWER OF" (mono 12px) sits above the headline.

&#x20; - The headline "\*\*Thinking\*\* / \*\*Machines\*\*" is `clamp(42px, 5.25vw, 92px)`, weight 400. Each line sits in its own box outlined with a 2px gradient border, with no fill.

&#x20; - "Thinking" is outlined orange→pink, with its bottom-right corner cut at 45°.

&#x20; - "Machines" is outlined amber→orange→pink.

\- \*\*Sub line:\*\* "Your personal expert in all crypto \& blockchain related topics." at 14.5px, bottom 3.6 %, left at 62 % + 18px so it stays clear of the pedestal.

\- \*\*Scroll link:\*\* "SCROLL" plus a down-arrow inside corner brackets at the bottom right. The arrow bobs 4px every 2s.

\- \*\*Bottom rule:\*\* a hairline from 50 % to the right edge at bottom 14 %.



\## Section 2: Product (100vh)



\- \*\*Tab carousel:\*\* a 74px strip near the top, starting at the 17 % guide.

&#x20; - It holds 10 tabs, each 33vw wide: a 68px number cell plus a label. The labels are:

&#x20;   1. AI Chatbot

&#x20;   2. NFT Generator

&#x20;   3. Smart-contract generator

&#x20;   4. Blockchain \& market analytics

&#x20;   5. AI Trading assistant

&#x20;   6. Code auditor

&#x20;   7. Chart \& technical analysis

&#x20;   8. Crypto news AI

&#x20;   9. Smart-contract auditor

&#x20;   10. AI Chatbot

&#x20; - Every 2.4s the strip slides one tab left (0.9s, `cubic-bezier(.65,0,.2,1)`).

&#x20; - The active tab gets a 1px frame and corner brackets with full-ink text. Later tabs stay at 14 % ink, and tabs that have passed fade out.

\- \*\*Headline (bottom left, `clamp(30px, 3.05vw, 54px)`):\*\*

&#x20; - A mono "··" above.

&#x20; - "Your Gateway", in a 1px rounded outline box.

&#x20; - "To Web3 AI" underneath.



\## Section 3: Reviews (100vh)



\- \*\*Header strip:\*\* 60px tall, near the top, with a hairline under it.

&#x20; - "TSTMNL" and the number "01" inside a small bracket.

&#x20; - A 56px square avatar, a dot, then the name.

&#x20; - The role in dim mono.

\- \*\*Quote:\*\* left, top 26 %, 23vw wide, `clamp(20px, 2.3vw, 40px)`, line height 1.19.

&#x20; - Under it, "Try for yourself (Click Here)", with a 1px rule on its left.

\- \*\*Arrows:\*\* ← → at the bottom left. Clicking one fades the name, role and quote out (0.45s, 10px drop), swaps them, then fades them back in.

\- \*\*Ghost:\*\* the next review shows as a 10 % ink ghost to the right of the 83 % guide.

\- \*\*Reviews (all fictional):\*\*

&#x20; 1. “Smart contract auditing has always been a bottleneck for our startups, Nova Agent solves this problem in seconds. (Ilan Brooks, Founder of Halden Capital)

&#x20; 2. Nova Agent is a vital asset for Web3 investors, simplifying the research process effortlessly. (Rhea Okafor, Co-founder of Tessel Network)

&#x20; 3. “The fastest way we have found to go from an idea to a deployable token contract. (Mara Elling, CTO at Northline Labs)

\- \*\*Footer:\*\* 30vh, centred mono "NOVA AGENT · 2026".



\## Reveal



Every block has class `.rv`: opacity 0 and translateY 26px. When its section first enters view (IntersectionObserver at .15), it eases in over 1s with `cubic-bezier(.2,.7,.2,1)`, staggered .1s, .2s, .3s and .4s.



\## The robot (three.js, fixed full-screen transparent canvas)



\### Renderer, environment and lights



\- \*\*Renderer:\*\* antialias, alpha, pixel ratio capped at 2, ACES Filmic tone mapping with exposure 1.05, sRGB output, soft PCF shadows.

\- \*\*Environment:\*\* PMREM from `RoomEnvironment` (blur .04) at intensity .9.

\- \*\*Camera:\*\* perspective, 30° FOV.

\- \*\*Lights:\*\*

&#x20; - \*\*Hemisphere:\*\* sky `#fff6ee`, ground `#d9d2c8`, intensity .7.

&#x20; - \*\*Key:\*\* directional `#fff3e6` at 1.7 from (-3, 5, 4). Casts a 1024px shadow with radius 6 and bias -.0005.

&#x20; - \*\*Rim:\*\* directional `#fff0e6` at 1.2 from (4, 2, -4).

&#x20; - \*\*Fill:\*\* warm point light `#ff9a6a` at 2.2 from (-3.2, 1.2, .6), range 6.



\### Materials



| Material | Settings |

|---|---|

| Shell | MeshPhysical `#eeebe6`, roughness .38, clearcoat .45 (roughness .3) |

| Shell light | `#f8f6f2`, roughness .34, same clearcoat |

| Joints (dark) | `#1b1b1f`, roughness .55, metalness .3 |

| Deep dark | `#0f0f12` |

| Pedestal | `#2a2928`, roughness .9 |

| Ring | See below |



\*\*Ring:\*\* a 512px canvas conic gradient (pink #ff3d8b → coral #ff5a5f → orange #ff8a3d → amber #ffb347 → orange → coral → pink), used as both map and emissive map (emissive .22). Roughness .5, clearcoat .35.



\### Build (units)



\- \*\*Head:\*\* a group pivoting at y .78 (head centre at +.78 above the pivot).

&#x20; - Skull: rounded box 1.5 × 1.42 × 1.3, radius .2.

&#x20; - Dark back block: 1.28 × 1.14 × .9, set back. Scatter \~26 tiny dark "circuit" bars over its back and top.

&#x20; - Face ring: an extruded rounded-rect frame (outer 1.5 × 1.44, r .3; inner 1.08 × 1.02, r .2; depth .1; bevel .03) with the ring material, at z .6. Remap the UVs to the frame's bounds so the gradient wraps around it.

&#x20; - Bezel: an inner shell-light frame at z .62.

&#x20; - Screen: a rounded plate .9 × .84 at z .66. Glossy black with clearcoat 1, and the face canvas as its emissive map (intensity 1.6).

&#x20; - Ears: cylinder r .22 on both sides, with caps. On the right, a half-torus dark cable loops down.

\- \*\*Neck:\*\* a dark cylinder.

\- \*\*Torso:\*\* rounded box 1.22 × 1.12 × .92, r .24.

&#x20; - A shell-light chest-top slab.

&#x20; - Three small emissive LEDs on the chest: `#ff8a3d`, `#ff5a5f`, `#ff3d8b`.

&#x20; - Two dark vertical slots with dark half-torus lips above them.

&#x20; - A dark pelvis.

\- \*\*Arms:\*\* at each shoulder a dark ball, a shell upper arm, a dark elbow ball, then a forearm group holding a shell-light hand block and a thumb. Shoulders splay out by ±.16 rad; forearms bend by -.35.

\- \*\*Legs:\*\* a dark hip ball, a shell leg block, a dark ankle, and a shell-light foot.

\- \*\*Pedestal:\*\* a 1.7 × 1.6 × 1.7 box under the feet (y -2.22) that receives shadows.



\### Face canvas (512px)



\- Black fill. White shapes with a white glow (shadowBlur 18).

\- \*\*Eyes:\*\* two ellipses at (196, 262) and (316, 252), radius 30 × 38.

\- \*\*Blink:\*\* every 2.5–5.5s the eyes squash vertically to 10 % and back over .18s.

\- \*\*Quote mode:\*\* a single 560px "Arial Black" “ centred at (256, 400). When the mode changes, the new face fades in at +.05 alpha per frame.



\## Motion



\- \*\*Scroll:\*\* p = scrollY / innerHeight, clamped 0–2, smoothed by 8 % per frame. It blends three camera states with ease-in-out cubic:



| State | Camera z | Camera y | Look-at y | Body yaw | Head yaw / pitch / roll |

|---|---|---|---|---|---|

| Intro | 11.6 | 1.1 | .55 | -.42 | -.6 / .16 / .22 (tilted, looking left) |

| Product | 6.9 | 1.95 | 1.72 | -.2 | -.06 / .04 / 0 (close-up on the head) |

| Reviews | Same as Product | | | | |



\- The face switches to quote mode once smoothed p passes 1.55.

\- On screens under 900px, camera z is multiplied by 1.25.

\- \*\*Pointer:\*\* the normalised cursor, smoothed by 6 % per frame:

&#x20; - moves the camera ±.25 x and ∓.1 y,

&#x20; - adds .12 to body yaw,

&#x20; - adds .45 to head yaw and .18 to head pitch.

\- \*\*Idle:\*\*

&#x20; - the body bobs ±.02 (sin 1.4t),

&#x20; - the head sways slightly (pitch sin .9t × .02, roll sin .7t × .02),

&#x20; - the arms swing gently (shoulder sin(1.4t + side) × .05, forearm × .06).



\## Mobile (≤ 900px)



\- \*\*Hidden:\*\* the outer guides, the menu, the pad cell, the rail, the feature list and the ghost.

\- \*\*Layout:\*\*

&#x20; - The nav becomes logo + button.

&#x20; - The prompt box spans the width at top 18 %.

&#x20; - The headline and scroll link sit 16px from the edges.

\- \*\*Readability:\*\* the robot fills the screen, so the headline boxes, the "UNLEASH" line, the sub line, the "Gateway" lines, the quote and "Try for yourself" get a paper backing at `rgba(239,236,230,.88)`.



\## Notes



\- The brand, product names, token ($NOVA) and every person and company in the reviews are fictional. Don't use real brand names or logos.

