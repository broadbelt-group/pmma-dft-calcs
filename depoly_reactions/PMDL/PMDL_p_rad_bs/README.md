# PMDL - PMDL_p_rad_bs Transition State Workflow

This directory contains a complete transition state calculation workflow:

1. **01_reactant/**: Optimize reactant structure
2. **02_scan/**: Perform bond scan to find approximate TS
3. **03_ts_opt/**: Optimize transition state structure  
4. **04_products/**: Optimize product structures

## Bond Scan Parameters:
- Bond atoms: 5 - 12
- Distance range: 1.5 - 3.0 Å
- Steps: 20

## Usage:
```bash
# Run individual steps
python scripts/submit_job.py transition_states_new/PMDL/PMDL_p_rad_bs/01_reactant/
python scripts/submit_job.py transition_states_new/PMDL/PMDL_p_rad_bs/02_scan/
python scripts/submit_job.py transition_states_new/PMDL/PMDL_p_rad_bs/03_ts_opt/
python scripts/submit_job.py transition_states_new/PMDL/PMDL_p_rad_bs/04_products/

# Or run entire workflow automatically
python scripts/workflow_manager.py ts transition_states_new/PMDL/PMDL_p_rad_bs/
```
