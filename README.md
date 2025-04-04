# Tölvera

> ⭐️ Tölvera has been selected for Mozilla's first Builders Accelerator! [Read the announcement](https://blog.mozilla.org/en/mozilla/14-ai-projects-to-watch-mozillas-first-builders-accelerator-cohort-kicks-off/) and join our [Discord](https://discord.gg/ER7tWds9vM)!

![type:video](https://www.youtube.com/embed/BmoinLR8Otc)

[Tölvera](https://tolvera.is) is a Python library designed for [composing together](https://arxiv.org/abs/2303.06777) and interacting with [basal](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2019.0750) [agencies](https://link.springer.com/article/10.1007/s00018-023-04790-z), inspired by fields such as artificial life (ALife) and self-organising systems. 
It provides creative coding-style APIs that allow users to combine and compose various built-in behaviours, such as flocking, slime mold growth, and swarming, and also author their own. 

With built-in support for Open Sound Control (OSC) via [iipyper](https://github.com/Intelligent-Instruments-Lab/iipyper) and interactive machine learning (IML) via [anguilla](https://github.com/Intelligent-Instruments-Lab/anguilla), Tölvera interfaces with and rapidly maps onto existing creative computing software and hardware, striving to be both an accessible and powerful tool for exploring [diverse intelligence](https://www.frontiersin.org/articles/10.3389/fnsys.2022.768201/full) in artistic contexts.

Inspired by our lab's location in Iceland, the word Tölvera is an Icelandic [kenning](https://en.wikipedia.org/wiki/Kenning) based on _tölva_ meaning computer, from _tala_ (number) and _völva_ (prophetess), and _vera_ (being), composed together as _number being_.

We have employed Tölvera in various collaborative artistic works, including musical performances, compositions, and multimedia installations (see [`references.bib`](https://github.com/Intelligent-Instruments-Lab/tolvera/blob/main/references.bib) for peer-reviewed publications).
Tölvera's role in these pieces has mainly been "mappable behaviour engine", where interface inputs can control Tölvera programs, and Tölvera runtime data can control interface outputs, in practically any combination.
In this way, and to controllable degrees, Tölvera can contribute to the underlying dynamics of a given interactive scenario.
It can also add a [visual component](https://www.youtube.com/watch?v=W2c8vFmdANY), and equally has been used without projection in [other works](https://marcodonnarumma.com/works/ex-silens/).

Tölvera makes use of [Taichi](https://www.taichi-lang.org/), a domain-specific language embedded in Python that enables parallelisation, and is experimental software subject to change.

We would be happy to have you join us on our [Discord](https://discord.gg/ER7tWds9vM) server!

## Showcase & Examples

Examples can be found at [iil-examples/tolvera](https://github.com/Intelligent-Instruments-Lab/iil-examples/tree/main/tolvera).
See also the [guide](https://afhverjuekki.github.io/tolvera/guide), [reference](https://afhverjuekki.github.io/tolvera/reference/tolvera/context) and [experiments](https://afhverjuekki.github.io/tolvera/experiments) pages.

[Visit the YouTube Playlist](https://www.youtube.com/embed/ahSXjnYHZLU?&list=PL8bdQleKUA1vNez5gw-pfQB21Q1-vHn3x) (if you'd like to add a video, please get in touch).

![type:video](https://www.youtube.com/embed/ahSXjnYHZLU?&list=PL8bdQleKUA1vNez5gw-pfQB21Q1-vHn3x)

<!-- [![](assets/images/tolvera.jpg)](https://www.youtube.com/watch?v=ahSXjnYHZLU&list=PL8bdQleKUA1vNez5gw-pfQB21Q1-vHn3x&pp=gAQBiAQB) -->

## Install

Taichi [supports numerous operating systems and backends](https://docs.taichi-lang.org/docs/hello_world#supported-systems-and-backends).
If you plan on using Vulkan for graphics (recommended for macOS), you may need to [install the Vulkan SDK](https://docs.taichi-lang.org/docs/hello_world#supported-systems-and-backends) first and restart your machine.

Tölvera is [registered on PyPI](https://pypi.org/project/tolvera) and can be installed via a Python package manager such as `pip`:

```sh
pip install tolvera
```

## Develop

For development, we use [`poetry`](https://python-poetry.org/).
Fork/clone this repository and install the package with `poetry:

```sh
git clone https://github.com/Intelligent-Instruments-Lab/tolvera # (or clone your own fork)
cd tolvera
poetry install
```

## Documentation

Documentation is written using [MkDocs](https://www.mkdocs.org/).

```sh
mkdocs serve # serve the docs locally
mkdocs build # build the docs
mkdocs gh-deploy # deploy via github pages
```

## Known Issues & Limitations

- Tölvera does not support Intel-based Apple devices (due to [`anguilla`](https://github.com/Intelligent-Instruments-Lab/anguilla)'s FAISS dependency, and Mediapipe not supporting Intel Macs).
- On macOS, [an OpenMP issue](https://github.com/pytorch/pytorch/issues/78490) may prevent Tölvera programs from running, which can be addressed by adding the following environment variable:
```sh
export KMP_DUPLICATE_LIB_OK=TRUE
```
- Sonification via [SignalFlow](https://signalflow.dev) does not work on Windows.
- Mediapipe versions [may need to be downgraded](https://github.com/google/mediapipe/issues/5168) in order to work on macOS and Windows.
- `OSError: Could not find any hidapi library`: this is due to the DualSense (PS5 controller) class. On macOS you can `brew install hidapi` and it should work. 

## Contribute

We welcome [Pull Requests](https://github.com/Intelligent-Instruments-Lab/tolvera/pulls) across all areas of the project:

- Addressing [Issues](https://github.com/Intelligent-Instruments-Lab/tolvera/issues)
- Adding features (see [Issues](https://github.com/Intelligent-Instruments-Lab/tolvera/issues) and [Discussion](https://github.com/Intelligent-Instruments-Lab/tolvera/discussion))
- [Examples](https://github.com/Intelligent-Instruments-Lab/iil-examples/tree/main/tolvera)
- [Tests](https://github.com/afhverjuekki/tolvera)
- [Documentation](https://afhverjuekki.github.io/tolvera/)

## Community

To discuss Tölvera with developers and other users:

- Use GitHub [Issues](https://github.com/Intelligent-Instruments-Lab/tolvera/issues) to report bugs and make specific feature requests.
- Use GitHub [Discussions](https://github.com/Intelligent-Instruments-Lab/tolvera/discussions) to share ideas and ask questions.
- Use [Discord](https://discord.gg/ER7tWds9vM) for further support, sharing your work, and general chat.

Across the project, we follow the [Berlin Code of Conduct](https://berlincodeofconduct.org/). 
Please get in touch if you experience or witness any conduct issues.

## Roadmap

See [Discussion](https://github.com/Intelligent-Instruments-Lab/tolvera/discussion).

## Citation

Tölvera is being written about and used in a number of contexts (see [references.bib](https://github.com/Intelligent-Instruments-Lab/tolvera/blob/main/references.bib)).
The current canonical citation is our [NIME 2024](https://www.nime2024.org/) paper:

```bibtex
@inproceedings{armitageTolveraComposingBasal2024,
  title = {T{\"o}lvera: {{Composing With Basal Agencies}}},
  booktitle = {Proc. {{New Interfaces}} for {{Musical Expression}}},
  author = {Armitage, Jack and Shepardson, Victor and Magnusson, Thor},
  year = {2024},
  address = {Utrecht, NL},
}
```

## Inspiration

- [Michael Levin](https://en.wikipedia.org/wiki/Michael_Levin_(biologist))
- [SwissGL](https://swiss.gl)
- [Lenia](https://chakazul.github.io/lenia.html)
- Particle Life (attributed to various, see for example [Clusters](https://www.ventrella.com/Clusters/))
- [Journey to the Microcosmos](https://www.youtube.com/@journeytomicro)
- [Complexity Explorables](https://www.complexity-explorables.org/)

## Contact

Tölvera is developed by [Jack Armitage](https://jackarmitage.com).

## Acknowledgements

We thank the Taichi community for their project that makes Tölvera possible.

Tölvera was originally created at the [Intelligent Instruments Lab](https://iil.is).
