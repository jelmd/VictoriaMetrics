# VictoriaMetrics

This repository is a fork of [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics).

Its purpose is to provide structured feedback on upstream releases and to
maintain enhancements in separate branches, enabling straightforward
integration into the original repository via GitHub pull requests or comparable
contribution mechanisms.

# Branches
The **patched** branch consolidates all relevant enhancements and
branches maintained in this repository into a single, unified version.

It is currently based on v1.136.0 + bugfixes with the following branches merged:
- [lnf_make_patch](https://github.com/jelmd/VictoriaMetrics/tree/lnf_make_patch)
- [log_aggregation](https://github.com/jelmd/VictoriaMetrics/tree/log_aggregation)
- [proc_clean](https://github.com/jelmd/VictoriaMetrics/tree/proc_cleanup)
- [easier_relabel_debug](https://github.com/jelmd/VictoriaMetrics/tree/easier_relabel_debug)

Periodically, this branch is synchronized with the upstream repository.
If the divergence becomes substantial, it is renamed to patched-_oldVersion_, and a new patched branch is created from master.

The **master** branch simply tracks the **upstream**.


All other branches are either work in progress (WIP), or obsolete or
experimental (e.g., case studies), and should not be used in production.


# Versioning

To clearly distinguish this build from the official release, an
extended versioning scheme is used:
- The fourth and fifth version components correspond to the last two digits of
  the most recent LTS release of [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics/releases).
- The sixth component indicates the incremental update number (version)
  of the **patched** branch.

**NOTE**: The original [README.md](https://github.com/VictoriaMetrics/VictoriaMetrics/blob/master/README.md) has been renamed to `README-orig.md` to ensure that GitHub displays
this document by default, as there is currently no alternative mechanism to
control the default README display behavior.
