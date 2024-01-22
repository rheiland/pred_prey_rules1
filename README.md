This model attempts to model a type of predator-prey where, if the prey clump together,
the predator is unable to eat them. This is accomplished by detecting how many (spring) attachments
there are to each prey and, if there are greater than some threshold, transform the "prey"
cell type into "prey_big". (Note the values for "attachment rate" in Cell Types|Mechanics for
the different cell types). A single Rule transforms "prey" to "prey_big" if the number of 
attachments (Custom Data of cell types) exceeds a threshold.

Note that it is necessary to save the number of spring attachments into a custom data variable in custom.cpp (since that value is not exposed in the rules (yet)).
```
void phenotype_function( Cell* pCell, Phenotype& phenotype, double dt )
{
    pCell->custom_data["num_attached"] = pCell->state.spring_attachments.size();
	return;	 
}
```

See the 'images' folder for some output screenshots.
