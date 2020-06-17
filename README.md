## Summary

ETL pipeline used by NHM Informatics to resolve taxonomic names gathered from biodiversity papers as part of the PREDICTS2 project. The GBIF species endpoint is used to resolve more straightforward names (inc. synonyms) and to identify names requiring manual resolution by an appropriately qualified human. 

The conceptual overview of this process is shown in high_level_process.jpg. Details of the NHM implementation of this project is in the predicts_name_resolution.pdf and ETL diagram.jpg.

## Notes + caveats

 - Name resolution for this project was completed in **September 2019**, so running the same queries against the current version of the GBIF backbone may produce different results. 
 - This process is an example of a local integration with the **GBIF taxonomic backbone**: all the clever stuff around name disambiguation etc. is their work and you can try it out in-browser here: https://www.gbif.org/tools/species-lookup (API endpoint in docs)
 - The .ktl file in this repo is intended for use as an example of local data-cleaning via GBIF-mediated data + services, rather than a production ready script.
 - Database connection details have been scrubbed from name_resolution.ktr. Database model + manual resolution sheet are out of scope of this repo, but happy to share on request. 
