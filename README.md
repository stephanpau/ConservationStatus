# ConservationStatus
## Purpose
This data compilation was made to evaluate the evaluation state of elasmobranchs (sharks, skates and rays) present in French waters. As there was only one national French IUCN evaluation available for these species, we wanted to have an overview of other evaluations (IUCN and conventions) for all the species.    
It is composed of 5 scripts :  
1. **01_IUCN_status**: this script produces a table containing the historical evolution of IUCN status by species and region. The first columns summarise the essential information. They are followed by column with years as names and the status as content. This allows the user to have more detailed information, e.g. if they want to look for the evolution of a specific species in a specific region.  
2. **02_Convention_appendices**: this table summarises which species are cited in which convention appendices (Bern, Barcelona, Bonn, CITES).  
3. **03_OSPAR_status**: This is the OSPAR status information extracted from their website. As the format is very different than the IUCN status and there are much fewer species evaluated, I decided to keep it separated from the IUCN table.  
4. **04_ICES_advice**: This script extracts information from the advice files available on the ICES website.  
5. **05_Export_html_tables**: Finally, this file styles and exports nice html tables of the results.  

## How to reuse it
### For elasmobranchs
The IUCN historical table will be updated automatically with new info available on the IUCN website. The **french IUCN list** and the **national lists** will need to be changed to the newest file available on the net. If you put the files in the "data" order of the repository and give them the same names as the old ones, it should work just the same. *Just check they are in the same format.*

### For other species
You can run this code easily for other species by replacing the species_names list. The IUCN french list file won't be useful, as well as the Oegelund Nielsen df if you're not working on elasmobranchs. In a nutshell, the IUCN API part is the easiest to reuse to work on species other than elasmobranchs or fish in general.
