# Taxonomy

Taxonomy version 4. This file is the filing vocabulary for gororoba-documents-public and for its private sibling
gororoba-documents-private. Both repositories file every document at `<field>/<subject>/<file>`, using the fields and
subjects below. A subject folder exists in a repository only while that repository holds a file in it, so a
private-only subject has no public folder.

## Filing a document

1. **Establish the work.** Open the PDF and read its title page. A filename, an arXiv ID in a filename, or a DOI
   string is a claim to check, not proof of identity.
2. **Establish the rights of the exact bytes.** The public repository admits only these: a Creative Commons license
   of any variant, CC0, documented public-domain status, or another license that grants redistribution of those
   bytes. Everything else goes to the private repository.
3. **Choose the field and subject.** Use the scope rules and precedence order below. The primary question of the
   work decides; the mathematics a work uses along the way does not.
4. **Record the kind** in the manifest's `kind` column.
5. **Name the file** by the filename rules below.
6. **Add the manifest row** in the same commit as the file, and verify the checkout against the manifest.

## Fields

| Field | Scope |
|---|---|
| `mathematics` | Mathematical objects and theorems as the primary question. |
| `physics` | Physical systems, experiments and physical models, including quantum hardware and quantum information physics. |
| `computer-science` | Algorithms, complexity, languages, software, formal verification and learning systems. |
| `statistics` | Estimation, testing, inferential methodology and research reliability. |
| `engineering` | Engineered devices, signal processing, estimation and control of physical plants, manufacturing, system architecture. |
| `humanities` | Religion, language, culture and archival documents studied as human practice rather than as science. |
| `user_documentation` | Documents the owner authored in the workspace repositories: manuscripts, synthesis reports, cover letters and generated figures. Private-only: gororoba-documents-public holds no file in this field. |

A mathematical structure studied without a physical question belongs in mathematics, even when the work is posted
under math-ph or hep-th. A quantum algorithm or compiler belongs in computer science; the device that runs it
belongs in physics.

## Subjects

### mathematics

| Subject | Scope |
|---|---|
| `cayley-dickson` | The construction across dimensions, sedenions and higher algebras, their zero divisors, construction-specific loops. |
| `octonions` | Octonion and split-octonion algebra, G2, triality, integral octonions and octonionic geometry outside a whole-tower question. |
| `quaternions` | Quaternion-family algebra, orders, matrices and geometry, excluding dual extensions and function theory. |
| `dual-number-algebras` | Dual numbers and dual extensions of quaternion, octonion and higher algebras. |
| `hypercomplex-numbers` | Hyperbolic, perplex, hybrid and multicomplex systems and sequences outside the named families. |
| `nonassociative-algebra` | Composition, alternative, Jordan, Albert and Okubo algebras, general loops and quasigroups, cross-family theory. |
| `clifford-algebra` | Clifford and geometric algebra as the primary mathematical object. |
| `hypercomplex-analysis` | Function theory, regularity, power series and transforms over hypercomplex algebras. |
| `algebra-and-representation` | Associative, commutative and group algebra, representation and operadic algebra, generalized arithmetic such as wheels. |
| `geometry-and-topology` | Geometry, topology, homotopy and geometric structures whose question outranks a specific algebra family. |
| `combinatorics` | Graphs, designs, finite and polyhedral combinatorics, Hadamard matrices, mutually unbiased bases. |
| `number-theory` | Arithmetic, integer and prime structure, arithmetic bounds. |
| `analysis` | Real, complex and functional analysis, PDE, spectral analysis, numerical methods outside hypercomplex function theory. |
| `logic-and-foundations` | Foundational logic, type theory and proof theory. |
| `history` | Historical interpretation as the primary question, and historical treatises that no subject above covers. |
| `reference-and-bibliography` | Tables of contents, bibliographies and other finding aids. |

When subjects overlap, apply this precedence:

1. Function theory or transforms go to `hypercomplex-analysis`.
2. Dual extensions go to `dual-number-algebras`.
3. A specific family goes to `octonions` or `quaternions`.
4. A question about the whole doubling tower goes to `cayley-dickson`.
5. General nonassociative theory goes to `nonassociative-algebra`.

### physics

| Subject | Scope |
|---|---|
| `quantum-devices-control` | Processor hardware, gate, readout and control mechanisms, hardware noise mechanisms, device roadmaps. |
| `quantum-characterization` | Calibration, tomography, benchmarking, error estimation and mitigation, drift detection. |
| `quantum-communication-optics` | Quantum optical components, interference, memories, entanglement distribution, teleportation. |
| `quantum-error-correction` | Logical and physical protection, codes and code operations, protected subspaces. |
| `quantum-information-foundations` | Foundations, information and channel theory, open-system theory, entanglement criteria. |
| `quantum-simulation` | Simulation and emulation of physical systems on quantum devices. |
| `hypercomplex-physics` | Physical models formulated through hypercomplex, division or Clifford algebras; incidental notation does not qualify. |
| `gravitation` | General relativity, gravitational dynamics and waves, compact objects, direct tests of gravity. |
| `quantum-gravity-and-holography` | Quantum spacetime, strings and supergravity, holography, gravity-linked noncommutative geometry. |
| `particles-and-dark-matter` | Particle and nuclear phenomenology and experiment, neutrinos, dark sectors. |
| `astrophysics-and-cosmology` | Astrophysical systems, the heliosphere, observations, cosmological inference. |
| `condensed-matter` | Materials, magnets, transport, crystals, many-body and tensor-network questions about matter. |
| `optics-and-photonics` | Classical electromagnetic optics, metamaterials, resonances, coupled modes, optical analogues. |
| `field-theory` | Field dynamics, amplitudes, Casimir and negative-energy theory, mathematical physics about fields. |

### computer-science

| Subject | Scope |
|---|---|
| `quantum-algorithms` | Quantum algorithms, their complexity and classical simulation bounds. |
| `quantum-software-architecture` | Quantum languages, circuit rewriting and compilation, instruction sets, architecture, scheduling. |
| `programming-languages` | Language semantics, types, calculi and implementation outside quantum specialization. |
| `theorem-proving` | Proof assistants, automated proving, implementation-oriented formal verification. |
| `machine-learning` | Learning methods, neural models, training and evaluation, supporting datasets. |
| `algorithms-and-complexity` | Classical algorithms, hardness and complexity. |
| `optimization-and-decision-science` | Optimization and decision methods for planning and policy. |
| `systems` | Operating systems, CPU microarchitecture, calling conventions, assembly, system software. |

### statistics

| Subject | Scope |
|---|---|
| `inference` | Estimation, tests, probability bounds, confidence sequences, empirical Bayes, selective inference. |
| `reproducibility` | Research reliability, preregistration, reproducibility methodology. |

### engineering

| Subject | Scope |
|---|---|
| `signal-processing` | Signal and array estimation and reconstruction, including quaternion signal processing. |
| `control-and-estimation` | State and parameter estimation, control and identification of physical plants. |
| `devices` | Device designs and patents whose primary object is an engineered device. |
| `manufacturing` | Manufacturing and materials-processing capabilities and procedures. |
| `systems` | Engineering architecture and integration, digital twins, infrastructure. |

### humanities

| Subject | Scope |
|---|---|
| `culture-and-society` | Religion and its relation to technology and science, lexicography and linguistics, folklore and archival reports of anomalous phenomena. |

### user_documentation

Private-only field. gororoba-documents-private files the owner's own documents here; the public repository carries no
`user_documentation` folder.

| Subject | Scope |
|---|---|
| `manuscripts` | Papers, synthesis and formalism documents, cover letters. |
| `figures` | Plots and dependency graphs. |

## Kinds

The manifest's `kind` column records the publication kind; kinds do not appear in paths.

| Kind | Scope |
|---|---|
| `preprint` | arXiv or another preprint server, author or accepted manuscript, working paper. |
| `journal` | Journal or proceedings article in publisher layout, historical journal scans and whole issues. |
| `book` | Book, monograph, chapter, edited volume, historical treatise. |
| `lecture-notes` | Lecture and course notes, tutorials, slides, expository notes. |
| `thesis` | Master's or doctoral thesis. |
| `report` | Technical or design report, white paper, manual, documentation, roadmap, reconstruction binder. |
| `patent` | Patent or patent application. |
| `figure` | A generated plot, chart or graph. |

## Filenames

- A file stamped with an exact arXiv version takes that ID as its name: `2505.11747v3.pdf`. An old-style ID replaces
  its slash with a hyphen: `math-0404395v1.pdf`.
- Any other file keeps a truthful descriptive name: `author_year_short_title.pdf`, or `title-slug--<10 hex of
  sha256>.pdf` when the author and year are not established. A name that describes a different work than the bytes
  is renamed. A name that is truthful stays.
- Names use only letters, digits, `.`, `_` and `-`, and are unique within their folder regardless of case.
- A Markdown transcription sits beside its PDF under the same stem with `.md`, and starts with its source URL, the
  PDF's sha256 and its license line.
- Distinct bytes of one work, such as two arXiv versions or a preprint and its journal version, stay distinct files
  with distinct names.

## Adding a subject

A subject holds every work its scope rule covers, whatever the count. A new subject enters only for works that fail
every existing scope: write the slug and its scope rule into this file, raise the taxonomy version, then move the
files. The owner approves every change to this vocabulary before files move.
