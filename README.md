Typical usage                                                                                                               
AMAP F/R/FR/FE/RE/FRE Forward_seq.ab1 Reverse_seq.ab1 Exons.fasta AminoAcidReference.fasta Reference_seq.fasta              
Where:                                                                                                                      
'F' means you are giving only forward sequences for alignment                                                               
'R' means you are giving only reverse sequences for alignment                                                               
'FR' means you are giving both Forward and Reverse sequences for alignment                                                  
Adding 'E' to the argument will enable exon extraction based on supplied exon file, its translation and alignment with      
reference amino acid fasta file.                                                                                            
AMAP uses all the cores available from system for running BLAST.                                                            
For multiplex usage for n number of samples:                                                                                
Example:                                                                                                                    
n = 2; That is, Sample A and B.                                                                                             
Typical Usage for such a sceneario:                                                                                         
AMAP Forward_seq_Sample_A.ab1 Forward_seq_Sample_B.ab1 Reverse_seq_Sample_A.ab1 Reverse_seq_Sample_B.ab1 Reference_Seq.fasta
Reverse Sequence should not be reverse complemented, the software does it on it's own.                                      
Kindly note that SeaView will not be automatically launched in case of multiplex run.                                       
You can manually open the *._result.aln file to visualize the alignment.                                                    
Requirements:                                                                                                               
Linux/Unix System with EMBOSS, SEQTK, Python 3.x, BioPython, NCBI BLAST+ Suite & CLUSTALW2 installed.                       
Made and tested on Mac OS X 10.11.4 with Pyhton 3.4, BioPython 1.66, EMBOSS 6.5.7, SEQTK, CLUSTALW2 2.1                     
                                                                                                                            
Optional:                                                                                                                   
Make the code executable using "chmod +x AMAP" and copy it to your system's PATH for easy invoking it from any folder.      
                                                                                                                            
You can download these freely available softwares from the below given links:                                               
EMBOSS       : http://emboss.sourceforge.net/download/                                                                      
SEQTK        : https://github.com/lh3/seqtk                                                                                 
BioPython    : http://biopython.org/wiki/Main_Page                                                                          
SeaView      : http://doua.prabi.fr/software/seaview                                                                        
NCBI BLAST+  : ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/

EasyGUI (required for installer only) : http://easygui.sourceforge.net
                                                                                                                            
Description of results:                                                                                                     
*._Forward_Sequence_QC.fastq             : QC Trimmed Forward Sequence in FASTQ format.                                     
*._Reverse_Sequence_QC.fastq             : QC Trimmed Reverse complemented reverse sequence in FASTQ format.                
*._consensus.fasta                       : Consensus sequence in FASTA format.                                              
*._result.aln                            : Alignemnet of consensus with reference sequecne in ALN format.                   
*._result.fasta_report.txt               : CLustalW2 alignment report.                                                      
*.consensus_BLAST.txt                    : Simplified BLAST result between Exonic sequence and extracted exon.              
*.EXON_*                                 : Files related with Exon extraction.
Failed_Result.txt                        : List of sequences failing quality tests.  
                                                                                                                            
Thanks for using the program!                                                                                               
For any suggestions/queries please contact:                                                                                 
Aditya Singh                                                                                                                
Ph.D. Scholar                                                                                                               
Advanced Paediatrics Center                                                                                                 
Post Graduate Institute of Medical Education and Research                                                                   
Chandigarh, India                                                                                                           
