# Subject Info

The subjects in this atlas are comprised from two different datasets.

More information about the datasets can be found in Subject_Info.xlsx

**New Mexico Decedent Database**
* case###### file names
* 0 to 3 months old
* Various pathologies

**LUNGMAP Dataset**
* R#### file names
* 0 to 4 months old

# Atlas Info

Each subject folder has the following structure
* "boundaries"
  * "_boundaries_": cell array of each organ in the slice and their x/y boundary coordiantes
* "conductivities" -> "assigned_cond_files_run#"
  * "_organs_": cell array of each organ in the slice and their x/y boundary coordiantes
  * "_setup_info_": structure for the mesh, including the background conductivity value
  * "_assigned_conductivities_": complex array of the conductivity value for each organ in the list of "_organs_", skipping over the "Body" row
* "conductivity_matrices" -> "conductivity_matrices_run#"
  * "_gamma_": 201x201 complex matrix showing the conductivity value in each pixel
  * "_x_bdry_": x values around the perimeter of the body
  * "_y_bdry_": y values around the perimeter of the body
* "conductivity_matrices_64by64" -> "conductivity_matrices_64by64_run#"
  * "_Cond_64by64_": 64x64 complex matrix showing the conductivity value in each pixel
* "perimeters"
  * "_perimeter_mm_": double containing the circumference of the torso in mm
* "voltages" -> "voltage_files_run#"
  * "_voltages_": 16x15 complex matrix of the measured voltages on all 16 electrodes for the 15 applied current patterns
