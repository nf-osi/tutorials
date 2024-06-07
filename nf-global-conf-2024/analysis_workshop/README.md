## Analysis workshop materials  


![tme-role-immune-cells](https://github.com/nf-osi/tutorials/assets/32753274/64c5a272-1c37-4df2-a91f-e1de71af4141)

This contains materials for a basic analysis with data on the NF data portal, primarily developed for the CTF-sponsored NF Global Conference 2024. 
All are welcome to adapt/reuse! 
For more context, see the .html presentation.

The basic analysis idea, tumor deconvolution, is the same but we have two versions in R and Python as somewhat different implementations. 
(The one actually presented was `analysis.Rmd`.) 
To help you better understand the differences and whether the demo material matches a scenario/learning objective you're interested in, here's a comparison table:


|                    | analysis.Rmd     | analysis.ipynb |
| ----------------   | -------------    | ------------- |
| Target demographic | useRs            |  Pythonistas  |
| Target demo env   | [Cavatica](https://www.cavatica.org/), local  | [Google Colab](https://colab.research.google.com/)  |
| Example dataset   | [syn53140231](https://www.synapse.org/Synapse:syn53140231)  | [syn60263853](https://www.synapse.org/Synapse:syn60263853/datasets/)  |
| Dataset data     | transcript-level quant.sf | gene-level quant.sf 
| Dataset AR?     | no AR  | yes AR |
| Dataset funder  | CTF  | NTAP  |
| Primary package | [immunedeconv](https://github.com/omnideconv/immunedeconv)  | [TumorDecon](https://www.sciencedirect.com/science/article/pii/S2352711022000528) |
| Analysis method | CIBERSORT  | CIBERSORT |
| Code diff 1     | Slightly higher-level code because of reuse of available packages in richer ecosystem for some steps | Slightly lower-level code because having to implement helpers for lacking packages in ecosystem |
| Code diff 2   | 3 example figures total based on ggplot2  | 1 example figure total based on seaborn |


Abbreviations:

- **AR**: Access Restriction

## License

 <p xmlns:cc="http://creativecommons.org/ns#" >This work is licensed under <a href="https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""></a></p> 





