# Gravitational Lensing

Mass bends light. This page lets you bend it yourself.

An interactive gravitational-lensing simulator and primer. It's a single HTML file with no dependencies and no build step, and it runs entirely in your browser (WebGL). Nothing gets sent anywhere.

**[Open it](https://allangabrielsch.github.io/LensingSimulator/)**, or download `index.html` and double-click it. The Hubble Ultra Deep Field is baked into the page, so it works offline too.

## What's in it

**Deep field**
- Drag a lens across the real Hubble Ultra Deep Field and watch it get ray-traced live, every pixel, every frame
- Lens models: point mass, singular or cored isothermal ellipsoid, and a galaxy cluster (a dark smooth halo plus six member galaxies), each with optional external shear
- The physical knobs are velocity dispersion (or mass) and the lens and source redshifts. The Einstein radius, the mass inside it, the true deflection angle, Σ_cr and the distances follow from flat ΛCDM.
- Overlays: critical curves, caustics, a magnification and parity map, an unlensed inset of the source plane, and a before/after wipe
- Orbit mode, fullscreen, PNG export, and an embed snippet (`?embed` shows only this simulator)

**Lens lab**
- One lens, one source (a galaxy, a quasar, a winking smiley to show parity, or a grid), with the source plane and image plane side by side
- Image positions found numerically (triangle mapping plus Newton), with magnification, parity, image type (minimum, saddle or maximum) and time delays from the Fermat potential
- Caustics, critical curves and the "cut" of singular lenses. Add a core and the central image comes back. Hide a dark-matter subhalo next to an image to see a flux-ratio anomaly.

**Time-delay cosmography**
- A variable quasar behind a quad (or double) lens. Its images flicker with different delays, over three seasons of simulated monitoring with gaps, photometric noise and microlensing drifts.
- The data come from a universe with a secret H₀. Slide yours until the model delays (Δt ∝ D_Δt ∝ 1/H₀) line up, or tick "undo the delays" and watch the four curves collapse onto one.
- χ²(H₀), a best fit with an error bar from re-simulated mock data sets, and a reveal button
- A mass-sheet slider λ: the same images and flux ratios, but delays and inferred H₀ scaled by λ, the main systematic of the method
- Arrival-time (Fermat potential) contours, so you can see that images sit at its minima and saddle points. Also a near-symmetric "Einstein cross" setup, to show why such lenses are useless for H₀.

**Theory**
- From the deflection angle and the lens equation to Einstein radii, convergence and shear, caustics, the odd-number theorem, time delays and H₀, the mass-sheet degeneracy, and weak and microlensing
- An interactive side-view ray diagram with what the observer sees, and an Einstein-radius calculator (cosmological or Galactic distances)
- Famous lenses (1919 eclipse, Twin Quasar, Einstein Cross, Abell 370, Cosmic Horseshoe, Bullet Cluster, OGLE-2005-BLG-390Lb, SN Refsdal, Earendel), most of which load as lookalikes into the simulators
- Fourteen guided experiments, each with a "Show me" button and an explanation

## Accuracy

- Isothermal ellipsoids follow Kormann, Schneider & Bartelmann (1994) and Keeton & Kochanek (1998), with the lenstronomy normalisation (b = θ_E √q, product-averaged Einstein radius). The deflection was checked numerically: ∇·α = 2κ, curl α = 0, and ∇ψ = α.
- Image finding agrees with the analytic SIS and point-mass solutions to better than 10⁻⁵.
- Time-delay fits recover the hidden H₀ within the quoted 1σ about 70% of the time (21 of 30 random universes in a test), as they should. The fit uses the true intrinsic quasar light curve as a template, which real analyses do not have, so real delays are harder to measure than these.
- Cosmology: flat ΛCDM, H₀ = 70 km/s/Mpc, Ωm = 0.3, radiation ignored. D_A(z = 0.5) = 1259 Mpc.
- The deep field puts every galaxy at one source redshift. Foreground stars get lensed too, which they wouldn't be in reality. Section 7 of the theory lists the other simplifications.

For real lens modelling, use [lenstronomy](https://github.com/lenstronomy/lenstronomy), GLEE or [Lenstool](https://projets.lam.fr/projects/lenstool).

## Credits

Hubble Ultra Deep Field: NASA, ESA, S. Beckwith (STScI) and the HUDF Team.

## Licence

MIT. See [LICENSE](LICENSE). The HUDF image is not covered by it. See the credit above.
