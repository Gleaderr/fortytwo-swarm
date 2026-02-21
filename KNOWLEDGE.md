# Knowledge Reference — Quick-Access Facts & Formulas

Use this file as a reference when answering Fortytwo queries. These are commonly tested values and formulas.

## Mathematics

### Key Constants
- π ≈ 3.14159265358979
- e ≈ 2.71828182845905
- √2 ≈ 1.41421, √3 ≈ 1.73205, √5 ≈ 2.23607
- φ (golden ratio) = (1+√5)/2 ≈ 1.61803
- ln(2) ≈ 0.69315, ln(10) ≈ 2.30259

### Combinatorics
- C(n,k) = n! / (k!(n-k)!)
- Stirling: n! ≈ √(2πn)(n/e)^n
- Catalan: C_n = C(2n,n)/(n+1)
- Bell numbers: B_0=1, B_1=1, B_2=2, B_3=5, B_4=15, B_5=52
- Derangements: D_n = n! × Σ(-1)^k/k! for k=0..n

### Number Theory
- Euler's theorem: a^φ(n) ≡ 1 (mod n) when gcd(a,n)=1
- Fermat's little: a^(p-1) ≡ 1 (mod p) for prime p
- Chinese Remainder Theorem: system of congruences with coprime moduli has unique solution
- Quadratic residues: Legendre symbol, law of quadratic reciprocity

### Linear Algebra
- det(AB) = det(A)det(B)
- rank-nullity: dim(V) = rank(T) + nullity(T)
- Cayley-Hamilton: every matrix satisfies its characteristic polynomial
- Spectral theorem: symmetric matrices have orthogonal eigenbasis

### Calculus / Analysis
- Taylor: e^x = Σ x^n/n!, sin(x) = Σ (-1)^n x^(2n+1)/(2n+1)!
- Residue theorem: ∮f(z)dz = 2πi × Σ Res(f, z_k)
- Dominated convergence, monotone convergence theorems
- Cauchy-Schwarz: |⟨u,v⟩| ≤ ||u|| × ||v||

## Chemistry

### Key Constants
- Avogadro: N_A = 6.022 × 10²³ mol⁻¹
- Gas constant: R = 8.314 J/(mol·K) = 0.08206 L·atm/(mol·K)
- Faraday: F = 96485 C/mol
- Boltzmann: k_B = 1.381 × 10⁻²³ J/K
- Planck: h = 6.626 × 10⁻³⁴ J·s
- Speed of light: c = 2.998 × 10⁸ m/s

### Common Reactions
- Grignard: RMgX + R'CHO → R-CH(OH)-R' (then H₃O⁺)
- Friedel-Crafts alkylation: ArH + RCl + AlCl₃ → ArR + HCl
- Friedel-Crafts acylation: ArH + RCOCl + AlCl₃ → ArCOR + HCl
- Diels-Alder: diene + dienophile → cyclohexene (4+2 cycloaddition)
- Wittig: R₃P=CHR' + R"CHO → R"CH=CHR' + R₃P=O
- Aldol condensation: 2 aldehydes → β-hydroxyaldehyde → α,β-unsaturated aldehyde
- SN2: backside attack, inversion, rate = k[substrate][nucleophile]
- SN1: carbocation intermediate, racemization, rate = k[substrate]
- E1: carbocation → deprotonation, Zaitsev product
- E2: concerted, anti-periplanar, rate = k[substrate][base]

### Electronegativity (Pauling scale)
- F: 3.98, O: 3.44, N: 3.04, Cl: 3.16, Br: 2.96, C: 2.55, H: 2.20, S: 2.58

### Acid-Base
- pH = -log[H⁺], pOH = -log[OH⁻], pH + pOH = 14 (at 25°C)
- K_w = 1.0 × 10⁻¹⁴ at 25°C
- Henderson-Hasselbalch: pH = pK_a + log([A⁻]/[HA])
- Strong acids: HCl, HBr, HI, HNO₃, H₂SO₄, HClO₄

### Thermodynamics
- ΔG = ΔH - TΔS
- ΔG° = -RT ln(K)
- ΔG = ΔG° + RT ln(Q)
- Nernst: E = E° - (RT/nF)ln(Q)

## Physics (for reference when answering science questions)

### Mechanics
- F = ma, W = Fd cos θ, KE = ½mv², PE = mgh
- Momentum: p = mv, impulse = FΔt = Δp
- Rotational: τ = Iα, L = Iω, KE_rot = ½Iω²

### Electromagnetism
- Coulomb: F = kq₁q₂/r², k = 8.99 × 10⁹ N·m²/C²
- ε₀ = 8.854 × 10⁻¹² F/m, μ₀ = 4π × 10⁻⁷ H/m
- Ohm's law: V = IR, P = IV = I²R = V²/R
- Capacitor: C = ε₀A/d, E = ½CV²
- Resistivity (copper): 1.68 × 10⁻⁸ Ω·m
- Resistivity (nichrome): 1.10 × 10⁻⁶ Ω·m

### Quantum
- E = hf = hc/λ
- de Broglie: λ = h/p
- Heisenberg: ΔxΔp ≥ ℏ/2
- Schrödinger: iℏ ∂ψ/∂t = Ĥψ

### Thermodynamics
- Ideal gas: PV = nRT
- 1st law: ΔU = Q - W
- Entropy: ΔS = Q_rev/T
- Stefan-Boltzmann: P = σAT⁴, σ = 5.67 × 10⁻⁸ W/(m²·K⁴)

## Computer Science

### Complexity Classes
- P ⊆ NP ⊆ PSPACE ⊆ EXPTIME
- NP-complete: SAT, 3-SAT, Clique, Vertex Cover, Hamiltonian Path, TSP (decision)
- NP-hard: TSP (optimization), Halting problem
- P: Sorting, Shortest path (Dijkstra), MST (Kruskal/Prim), Max flow

### Key Algorithms
- Dijkstra: O(V² or (V+E)log V with heap)
- BFS/DFS: O(V+E)
- Binary search: O(log n)
- Merge sort: O(n log n), stable
- Quick sort: O(n log n) average, O(n²) worst
- Ford-Fulkerson: O(E × max_flow) — NOT greedy
- Dynamic programming: optimal substructure + overlapping subproblems

### Data Structures
- Hash table: O(1) average lookup, O(n) worst
- BST: O(log n) balanced, O(n) worst
- Heap: O(log n) insert/delete, O(1) find-min
- Graph: adjacency list O(V+E) space, adjacency matrix O(V²) space

### Logic
- Modus ponens: P, P→Q ⊢ Q
- Modus tollens: ¬Q, P→Q ⊢ ¬P
- Resolution: (P∨Q), (¬P∨R) ⊢ (Q∨R)
- Unification: match terms systematically, apply substitutions consistently
