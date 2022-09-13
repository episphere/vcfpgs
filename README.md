# vcfpgs
GWAS (VCF,PGS) risk calculator

Pseudo code:

Def VCFPGS():
	
	FETCH PGS scores
		
		WRITE PGS RSID/CHR:POS:Alt:REF to .score txt file 
	
	READ VCF
	
		For line in VCF.gz Decompress and READ
		
			IF line contains RSID or CHR:POS:Alt:REF then STORE line or WRITE Line to .txt file
		
				ELSE: delete line from VCF
				
			For each PGS:
			
			Take Remaining lines in VCF and calculate summation of beta’s x effect for each PGS_ID
	
		Write risk for each PGS_id and Individual in VCF to output.file
	
	RETURN report and/or visual of PGS for each cancer PGS in catalog


To do:
 1. Determine how to read and parse gzipped VCF, while optimizing the memory required to decompress. 
