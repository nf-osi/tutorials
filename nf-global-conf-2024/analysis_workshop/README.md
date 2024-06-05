## Analysis workshop materials  


This contains materials for a basic analysis with data on the NF data portal, primarily developed for the CTF-sponsored NF Global Conference 2024. 
All are welcome to adapt/reuse! 
For more context, see the .html presentation.

The basic analysis idea, tumor deconvolution, is the same but we have two versions in R and Python as somewhat different implementations. 
(The one actually presented was `analysis.Rmd`.) 
To help you better understand the differences and whether the demo material matches a scenario/learning objective you're interested in, here's a comparison table:


|                    | analysis.Rmd     | analysis.ipynb |
| ----------------   | -------------    | ------------- |
| Target language demographic | useRs            |  Pythonistas  |
| Target demo env   | Cavatica, local  | Google Colab  |
| Example dataset   | syn123  | syn456  |
| Dataset data      | RNA-seq transcript-level quant.sf | RNA-seq gene-level quant.sf 
| Dataset AR?     | no AR  | yes AR |
| Dataset funder  | CTF  | NTAP  |
| Primary package | immundeconv  | tumordecon |
| Analysis method | CIBERSORT  | CIBERSORT |
| Code diff 1     | Slightly higher-level code because of reuse of available packages in richer ecosystem for some steps | Slightly lower-level code because having to implement helpers for lacking packages in ecosystem |
| Code diff 2   | 3 example figures total based on ggplot2  | 1 example figure total based on seaborn |


Abbreviations:

- **AR**: Access Restriction






