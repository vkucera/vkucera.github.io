# Vít Kučera

High-energy physicist and enthusiastic programmer with an eye for detail and extensive experience in developing and optimising data analysis frameworks.
Proficient in C++, Python, and various data management tools on Linux platforms.
Ready to bring analytical skills and technical expertise.

## Project contributions (non-exhaustive)

### [O2Physics](https://github.com/AliceO2Group/O2Physics) and [O2](https://github.com/AliceO2Group/AliceO2)

Analysis framework of the [ALICE](https://alice-collaboration.web.cern.ch/) experiment at [CERN](https://home.cern/)

- Core of the [heavy-flavour analysis framework](https://github.com/AliceO2Group/O2Physics/tree/master/PWGHF)
  - Designed, developed and [documented](https://aliceo2group.github.io/analysis-framework/docs/advanced-specifics/pwghf.html) a new framework for reconstruction, identification and analysis of heavy-flavour particles.
  - Coordinated a team of tens of contributors.
  - Selected contributions:
    - [`HfHelper`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/Core/HfHelper.h) - Helper class for calculations of properties of heavy-flavour decay candidates.
    - [`utilsEvSelHf`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/Utils/utilsEvSelHf.h) - Utilities for event selection.
    - [`pidCreator`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/TableProducer/pidCreator.cxx) - Workflow to produce particle identification flags combined from several detectors.
    - [`DerivedTables`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/DataModel/DerivedTables.h) - Definition of the self-contained derived analysis data format.
    - [`utilsDerivedData`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/Utils/utilsDerivedData.h) - Utilities for production of self-contained derived analysis data.
    - [`DecayChannels`](https://github.com/AliceO2Group/O2Physics/blob/master/PWGHF/Core/DecayChannels.h) - Definitions of decay channels relevant in reconstructed data and simulations.
- Utilities
  - [`RecoDecay`](https://github.com/AliceO2Group/O2Physics/blob/master/Common/Core/RecoDecay.h) - Methods for calculating properties of reconstructed decays.
  - [`TrackSelectorPID`](https://github.com/AliceO2Group/O2Physics/blob/master/Common/Core/TrackSelectorPID.h) - Class for track selection using particle identification detectors.
  - [`trackUtilities`](https://github.com/AliceO2Group/O2Physics/blob/master/Common/Core/trackUtilities.h) - Utilities for manipulating parameters of tracks and vertices.
  - [`PhysicsConstants`](https://github.com/AliceO2Group/AliceO2/blob/dev/Common/Constants/include/CommonConstants/PhysicsConstants.h) - Definitions of particle codes and masses.
- Productivity tools
  - [Dependency finder](https://aliceo2group.github.io/analysis-framework/docs/tools/dependencyFinder.html) - Automated identification of missing components of crashing analyses.
  - [Shell rc utilities](https://aliceo2group.github.io/analysis-framework/docs/tools/#shell-rc-utilities) - Helper functions for recompilation and debugging.
- Code quality enhancement
  - Systematically fixed compilation warnings and set CMake flags to treat them as errors in CI compilation tests.
  - Configured and used cpplint and cppcheck to find and fix bugs.
  - [O2 linter](https://aliceo2group.github.io/analysis-framework/docs/tools/o2linter.html) - Linter to detect framework-specific (and some general C++) issues in the code.
    - Integrated into CI and Visual Studio Code.
  - Cleaned up header dependencies.
    - Applied ["Include what you use"](https://include-what-you-use.org/) with clang-tidy.
    - [Configured](https://github.com/AliceO2Group/O2Physics/pull/11448) and used clang-format to sort and group `#include` directives.
    - Wrote an awk script to fix include style.
    - Proposed to add header compilation in the CI build tests.
  - [Configured](https://github.com/AliceO2Group/O2Physics/pull/11616) and used clang-tidy to check and fix identifier names according to the project naming conventions.
- Continuous integration
  - Set up GitHub action workflows for O2 linter and [MegaLinter](https://megalinter.io/).
  - [PR title prefix checker](https://github.com/AliceO2Group/O2Physics/blob/master/.github/workflows/labeler.yml) - GitHub action to create or check a PR title prefix based on the PR labels.
  - Set up the GitHub repository to suggest the PR title as the default merge commit title.
  - Set up [pre-commit hooks](https://github.com/AliceO2Group/O2Physics/blob/master/.pre-commit-config.yaml) for formatting and linting.
  - Configured [dependabot](https://github.com/AliceO2Group/O2Physics/blob/master/.github/dependabot.yml) for automated scheduled updates of GitHub actions.
- Knowledge sharing and user support
  - Organised a hackathon and hands-on sessions at three collaboration-wide tutorial events for the new analysers.
  - Provides user support to analysers.
  - Initiated creation of an announcement channel to share important news affecting analysers in the community.
  - [Documentation](https://aliceo2group.github.io/analysis-framework/)
    - [Installation instructions](https://aliceo2group.github.io/analysis-framework/docs/gettingstarted/installing.html)
    - [Troubleshooting](https://aliceo2group.github.io/analysis-framework/docs/troubleshooting/)
    - [Tools](https://aliceo2group.github.io/analysis-framework/docs/tools/)
    - [Glossary](https://aliceo2group.github.io/analysis-framework/docs/glossary/)
    - [Heavy-flavour physics working group](https://aliceo2group.github.io/analysis-framework/docs/advanced-specifics/pwghf.html)
  - [Setup diagnostic tool](https://aliceo2group.github.io/analysis-framework/docs/tools/#setup-diagnostic-tool) for helping users remotely with their installations and framework setup.

### [Run 3 analysis validation framework](https://github.com/AliceO2Group/Run3AnalysisValidation)

Framework for automated parallelised local execution, testing and validation of any O2Physics analysis code on large local data samples.

Developed to faciliate validation of new O2Physics code against the software used in the previous periods of LHC data taking.

- Author, developer, maintainer.
- Among several other utilities, it includes a [maintenance script](https://github.com/AliceO2Group/Run3AnalysisValidation?tab=readme-ov-file#keep-your-repositories-and-installations-up-to-date-and-clean) for automated maintenance of Git repositories and builds of development packages.

### [MachineLearningHEP](https://github.com/alisw/MachineLearningHEP)

Package for high-energy physicists to perform optimisation of rare signals produced in ultra-relativistic proton-proton and heavy-ion collisions.

- Analysis code
  - [Variation script](https://github.com/alisw/MachineLearningHEP/blob/run3/machine_learning_hep/do_variations.py) to run the analysis with variations of parameters to assess systematic uncertainties of the results.
  - Plotting utilities for preparation of figures for publications.
- [Comparison tool](https://github.com/alisw/MachineLearningHEP/blob/run3/machine_learning_hep/utils/compare_root_files.py) for flexible numeric and visual comparison of objects in two output files and result validation.
- Continuous integration
  - Set up [pre-commit hooks](https://github.com/alisw/MachineLearningHEP/blob/run3/.pre-commit-config.yaml) for formatting and linting.
  - Configured dependabot for automated scheduled updates of GitHub actions.
  - Set up GitHub action workflows for [MegaLinter](https://megalinter.io/).
