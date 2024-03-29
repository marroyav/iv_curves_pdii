# Automatization of IV Curves for ProtoDUNE 2 Using DAPHNE 2
## Usage
It is NOT necessary to be within a DUNE DAQ environment to execute the current code. NEvertheless, as it is needed for most of the analysis tools I encourage the user to profit from the use of the DAQ env. A full description is available [here](https://dune-daq-sw.readthedocs.io/en/latest/packages/daq-buildtools/#setup-of-daq-buildtools), but in summary,
```bash
source /cvmfs/dunedaq.opensciencegrid.org/setup_dunedaq.sh
setup_dbt latest

dbt-create -nc fddaq_latest <workarea>
cd <workarea>
source env.sh
```
The `-n` flag will fetch an environment that is currently in development and may be unstable. If it is unstable, one can drop `-n` or use an earlier date. The `-c` flag is necessary to clone the Python environment.

Now that we are in a DUNE-DAQ working environment, we still need a few more Python libraries. This can be done with
```bash
pip install -r requirements.txt
```
This will also build this repository's custom `ivtools` Python package. For the moment, this package can be used to collect information to make analysis of the IV curves of the PD Modules at ProtoDUNE II. 
