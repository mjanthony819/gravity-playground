# gravity playground

Click and drag to fling planets into orbit — a small n-body gravity sandbox.

**Live demo:** https://mjanthony819.github.io/gravity-playground/

## what it does

- **click + drag** spawns a planet; the drag arrow sets its velocity
- mass slider, sim-speed slider, trails toggle
- **merge on collide** — collisions are perfectly inelastic and conserve mass + momentum
- presets: a mini solar system, binary stars, the famous three-body **figure-8** (Chenciner–Montgomery orbit, verified numerically), and a 120-body accretion disk
- light/dark theme with a starfield

## the physics

Newton's law of gravitation between every pair of bodies (O(n²), fine for a few hundred bodies), integrated with **kick-drift-kick leapfrog** — a symplectic scheme that conserves energy over long runs, which is why orbits don't spiral in or decay. A small softening term keeps near-misses from producing absurd accelerations. Presets zero the total momentum so the system doesn't drift off-screen.

## stack

Single `index.html` — vanilla JS + canvas, no libraries, no build step. Hosted on GitHub Pages.

## run locally

Open `index.html` in a browser.

---

Built with AI assistance (design and direction by [@mjanthony819](https://github.com/mjanthony819)).
