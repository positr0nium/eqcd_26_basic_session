# Qrisp Basics: Eclipse Qrisp Community Day 2026

Materials for the basic workshop at the [Eclipse Qrisp Community Day](https://qrisp.eu/general/community_day.html),
29 October 2026, Fraunhofer FOKUS, Berlin.

The workshop has two parts: an introduction to the Qrisp programming model, followed by a 30-minute coding
session in which you simulate the double-slit experiment.

## Contents

| File                                         | Description                                 |
| -------------------------------------------- | ------------------------------------------- |
| `slides.pdf`                                 | Slides of the introduction                  |
| `coding_session/double_slit_exercises.ipynb` | Notebook for the coding session             |
| `coding_session/double_slit_solutions.ipynb` | The same notebook with all exercises solved |

## Setup

Qrisp needs **Python 3.11 to 3.13**. Install it together with Jupyter, ideally in a fresh virtual environment:

```bash
python -m venv qrisp-env
source qrisp-env/bin/activate        # Windows: qrisp-env\Scripts\activate
pip install qrisp jupyter
```

Then get this repository and open the exercise notebook:

```bash
git clone https://github.com/positr0nium/eqcd_26_basic_session.git
cd eqcd_26_basic_session
jupyter notebook coding_session/double_slit_exercises.ipynb
```

Without git, use **Code → Download ZIP** on this page.



## The coding session

1. Encode the position of a particle as a `QuantumFloat`.
2. Use comparisons to compute `QuantumBool`s that say whether a position lies inside a slit.
3. Build a slit oracle and let `@auto_uncompute` clean up the temporary qubits.
4. Prepare the slit state with an exact version of Grover's algorithm.
5. Steer the beam with a phase ramp and apply the quantum Fourier transform to obtain the interference pattern.

Bonus exercises: a cheaper oracle built from multi-controlled phase gates, and your own Grover diffuser written
with `conjugate`.

## Links

- Qrisp documentation: <https://www.qrisp.eu/reference/>
- Qrisp on GitHub: <https://github.com/eclipse-qrisp/Qrisp>
- Questions during and after the workshop: the [Qrisp Discord](https://discord.gg/v5np7DeBaq)

## License

[Eclipse Public License 2.0](LICENSE)
