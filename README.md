This model attempts to model a type of predator-prey where, if the prey clump together,
the predator is unable to eat them. This is accomplished by detecting how (spring) attachments
there are to each prey and, if there are greater than some threshold, transform the "prey"
cell type into "prey_big". (Note the values for "attachment rate" in Cell Types|Mechanics for
the different cell types). A single Rule transforms "prey" to "prey_big" if the number of 
attachments (Custom Data of cell types) exceeds a threshold.

See the 'images' folder for some output screenshots.