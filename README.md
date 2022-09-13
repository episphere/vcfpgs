# vcfpgs
GWAS (VCF,PGS) risk calculator

Pseudo code:

Def VCFPGS():
	Read VCF
	Fetch PGS scores 
		For each PGS extract snps from vcf and summation of beta’s x effect alleles
		Store risk for each PGS_id
	Return report/visual of PGS for each cancer/trait 


To do:
 1. Determine how to read and parse gzipped VCF, while optimizing the memory required to decompress. 
