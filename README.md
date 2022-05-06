# ConservationStatus
## Purpose
This data compilation was made to evaluate the ecological state of elasmobranchs (sharks, skates and rays) present in French waters. As there was only one national French IUCN evaluation available for these species, we wanted to have an overview of other evaluations (IUCN and conventions) for all the species.

## Structure 
### Rmd scripts   
1. **01_IUCN_status**: this script produces a table containing the historical evolution of IUCN status by species and region. The first columns summarise the essential information: status evolution, year of last evaluation and last status. They are followed by columns with years as names and the status as value. This allows the user to have more detailed information, e.g. if they want to look for the evolution of a specific species in a specific region.  
2. **02_Convention_appendices**: the produced table summarises which species are cited in which convention appendices (Bern, Barcelona, Bonn, CITES).  
3. **03_OSPAR_status**: The script extracts the OSPAR status information from the OSPAR website for the species in the convention. As the format is very different than the IUCN status and there are much fewer species evaluated, I kept it separated from the IUCN table.  
4. **04_ICES_advice**: This script extracts advice history and stock categories from the advice files available on the ICES website.  
*All those outputs are stored in the "data" folder.*  
5. **05_Export_html_tables**: Finally, this script styles and exports nice html tables of the results. These html tables are stored separately in the "html_output" folder.  

### Folders
* data: stores all initial datasets needed for the analysis as w well as produced csv files.  
* ICES_advice: stores the pdf files downloaded from the 4th script and needed to extract the advice information.  
* html_output: stores all html tables and associated files.  

## How to reuse it
### For elasmobranchs
1. The IUCN historical table will be updated automatically with new info available on the IUCN website. The **french IUCN list** and the **national lists** will need to be changed to the newest file available on the net. If you put the files in the "data" order of the repository and give them the same names as the old ones, it should work just the same. (*Just check they are in the same format.*)  
2. For an update, you will have to look on the websites if new species were added.  
3. The code will work without updates unless OSPAR changes their website's architecture significantly.  
4. Same as for OSPAR, should work just the same unless they store their advice files differently.  
5. Is based on the 4 first scripts.  

### For other species
1. You can run this code very easily for other species by replacing the species_names list. The IUCN french list file won't be useful, as well as the Oegelund Nielsen df if you're not working on elasmobranchs.  
2. The information on elasmobranchs comes from a ready-to-use compilation. For other species, you'll have to either find a similar dataset or make your own.  
3. If you're working on species included in the OSPAR convention, it will work.  
4. The ICES script is easily reusable for other stocks, simply change the initial stock names' list.
