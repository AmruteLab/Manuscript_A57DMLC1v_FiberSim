# Manuscript_A57DMLC1v_FiberSim
1. Contains FiberSim simulation files used in the manuscript for A57D-MLC1v to generate the effect of reduced powertroke size and reduced detachment rate.

2. The following changes in the setup file were used to simulate the effect of reduced powerstroke size alone:

        "model": {
            "relative_to": "this_file",
            "options_file": "sim_options.json",
            "manipulations": {
                "base_model": "model.json",
                "generated_folder": "../generated",
                "adjustments": [
                    {
                        "variable": "m_kinetics",
                        "isotype": 1,
                        "state": 4,
                        "extension": 1,
                        "multipliers": [1, 0.68],
                        "output_type": "float"
                    },
                    {
                        "variable": "m_kinetics",
                        "isotype": 1,
                        "state": 4,
                        "transition": 1,
                        "parameter_number": 1,
                        "multipliers": [1.0, 0.79],
                        "output_type": "float"
                    }
                ]
            }

3. The following changes in the setup file were used to simulate the effect of reduced detachment rate alone:

        "model": {
            "relative_to": "this_file",
            "options_file": "sim_options.json",
            "manipulations": {
                "base_model": "model.json",
                "generated_folder": "../generated",
                "adjustments": [
                    {
                        "variable": "m_kinetics",
                        "isotype": 1,
                        "state": 4,
                        "extension": 1,
                        "multipliers": [1, 1],
                        "output_type": "float"
                    },
                    {
                        "variable": "m_kinetics",
                        "isotype": 1,
                        "state": 4,
                        "transition": 1,
                        "parameter_number": 1,
                        "multipliers": [1.0, 0.35],
                        "output_type": "float"
                    }
                ]
            }
