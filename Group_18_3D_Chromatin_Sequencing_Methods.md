Methods for Sequencing 3D Chromatin Structure
=============================================

### Introduction
------------

In recent years, it has become increasingly clear that distant regulatory elements are essential for the proper control of gene expression. It has also been shown that the structure of the genome is highly organized and segmented by a large array of factors, with these factors key to the determination of the activity of genes within various cell types. Technologies have been developed to probe these biological phenomena by sequencing DNA while preserving its 3D structure.

### Classic Chromosome Capture Methods
----------------------------------

#### 3C

Chromosome conformation capture, or 3C, is currently the leading method to study gene regulation and genomic organization. 3C technology is a one versus one method, meaning that it tests interactions between a candidate promoter-enhancer pair or a restricted set of genomic loci and requires prior knowledge of selected targets [(Hakim & Misteli, 2012)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6374129/).

There are four steps to the 3C method. First, chromatin segments near each other are crosslinked. Next, the genome is split into fragments using restriction enzymes. Third, linked chromatin segments are ligated together. Finally, the purified product after the ligation step is measured (Chowdhary, Kainth, & Gross, 2019). In 3C, PCR is performed after reversing crosslinking, with primers for the target and for the region theorized to interact with it.

| ![](https://lh5.googleusercontent.com/yWVptYnv8Pp5zdFd2MZVtGKjfYT4CIykQOa8GRZhPh6_KM-vlppqPERjOXFNql7pkj3DurFKwusNzQD9UG249oCDx54Cx8Rmyc7hc0HIab5Q6u_gya3-EfkpfoYKy0cHfM-eW6jroCj-1_NV8ciKZrdEQgwpdQEVw-iSrvGKniLL0q_6gNgvLI0tBtg1VQ) |
|:--:|
|3C schematic 
[(Chowdhary et al., 2020)](https://www.zotero.org/google-docs/?3DpGgv)|



#### 4C

Chromosome conformation capture on chip, or 4C, is sometimes referred to as circular 3C, because DNA is circularized during ligation. While 3C is a one versus one method, 4C can be considered a one versus all method, since rather than a pair of genomic loci, it can detect all the genomic regions interacting with the target region or identified region of interest [(Illumina, n.d)](https://www.zotero.org/google-docs/?XofpSS).  PCR is done on these circularized DNA molecules, with a primer for the target region, and the  results are then analyzed using microarrays. Like other methods, 4C suffers from PCR bias, for similar reasons. For instance, since 4C also uses restriction enzymes, the frequency of the sites recognized by the enzyme affects assay resolution [(Raviram et al., 2014)](https://www.zotero.org/google-docs/?BmpO4q).


| ![](https://lh5.googleusercontent.com/dUTKrX-PWGffTXDIz5WnboHdw1W0NFwm8YRTCMUD8vgsF7BsQAlRessG_aFI40Ag5suAQU-Bv-bX99LftaVwNUPX6d7t7n54Sl4Dq5tMjb7gEd5iofDCTJlHLavF853_McbolpVfvpPUAXvIYfqOmBNGCq99TlQ2OqDyujJ197ru0CaSlZca4t-Z0ah2EQ) |
|:--:|
| 4C schematic 
[(Krijger et al., 2020)](https://www.zotero.org/google-docs/?HogqKE) |

#### 5C

Chromosome conformation capture carbon copy, or 5C, is a many versus many method, because it can test all restriction fragments within a given region. A 3C library is generated first, and then during DNA ligation, oligonucleotides are also ligated to the reverse crosslinked products (Dostie, et al. 2006). The oligonucleotides are then selected for and sequenced. However, it is extremely hard to achieve widespread coverage using this method, for similar reasons as with 3C and 4C.

| ![](https://lh5.googleusercontent.com/KAxUdaN0jNg7YaAr3VBKlybbNMxdYQlcEO-s4I3u8bCvReyxcYdo0a2RjGohx8CFst0LmylFFw1qa3xm3QskbShST8AjwTKKF8nvG4tgBMQODaYT76Ktl6dsx8d5I7WImZZIYdS2NyWtbm1hl-bCbKZL0iolyK1h-aUiiLpytnQ0GtLpswBe9eGiog5Xgw) |
|:--:|
| 5C shematic 
[(Dostie et al., 2006)](https://www.zotero.org/google-docs/?t4ABJf) |


#### Hi-C

The Hi-C method extends the 3C approach to capture genome-wide interactions across all loci, rather than probing for interactions between two select regions. Following the cross-linking and restriction enzyme digestion steps seen in 3C, a biotin-labeled nucleotide is added to the sample; this nucleotide labels the blunt 5' overhangs left by the HindIII restriction enzyme, marking the fragments with biotin at their junction. Labeling the cross-linked DNA fragments in this way allows for the fragments initially close to each other in the nucleus to be preferentially ligated in the proximity ligation step. Next, the crosslink is reversed, the DNA is sheared and purified, and the biotin-containing fragments are selected using streptavidin beads. A Hi-C library is then created from the sample and is analyzed via parallel DNA sequencing (Berkum, et al., 2010).

The analysis produces a catalog of interacting fragments -- loci or chromosomal regions -- organized as an n-by-n contact matrix, the rows and columns of which correspond to partitioned chromosome regions. Visualizing the matrix as a heatmap can help elucidate the genome-wide chromosome structural features present, such as interactions between cis and trans regulatory elements, locus-specific chromatin components, topologically associating domains (TADs), and point interactions. Given a standard logarithmic (log base 2) presentation, a positive matrix value indicates that the number of observed contacts is greater than expected, while a negative number means that they are fewer than expected (Oluwadare, et al., 2019).


| ![](https://lh5.googleusercontent.com/F7Xxw0Vf7_awM194Az82vfX28foV0s77QRshvbUVthsFkm5-NDrcyjwTECNTM1ngpPadXj9G5vb-p3I-3RtMDsiPsnHMd6I1HtRq_jzHMvfSjX8eJoFSUNgyo-7T_uPSLDya0Adon2XCeAjNwO6nHWs6ZPkQE3Gs0lYWw9SnvgZvuZ-HiMa8WzCopdW9dA) |
|:--:|
|Interpretation of 3D chromosome features based on Hi-C heatmap 
(Rao et al., 2014)|


### Chromosome Capture Derivatives
------------------------------

As scientific technology progresses, there have been many derivatives developed to the 3C, 4C, 5C, and Hi-C chromosome capture techniques; these improvements aim to enhance various aspects of the original technology, such as reduced cost and noise reduction, though often with certain drawbacks accompanying these enhancements. Many such methods have been developed, so we will cover only a limited selection of techniques that have pioneered some significant improvements on the 3C family methods.

#### Capture-C

The Capture-C family of protocols uses oligonucleotide capture technology (OCT) to enrich for interactions of interest from 3C libraries. This method produces comparatively high-yield, high-capacity results when considered with 3C and other 3C variants.

Procedurally, Capture-C adds several steps to the 3C process to facilitate the pulldown of biotinylated fragments with magnetic beads. After a standard 3C process is performed, the 3C ligated fragments are sonicated, allowing the OTC protocol to enrich for the chosen regions of interest. These enriched fragments are then sequenced (Downes, et al. 2022).

As a result of this enhancement, Capture-C analysis is more sensitive to differentiating between cis and trans interactions and lower in PCR bias than standard 3C. Additionally, Capture-C sees a reduction in cost compared to classic 3C, as the technology allows for lower required sample input (Illumina, n.d.).

#### Micro-C

Micro-C is a derivative of Hi-C that uses the micrococcal nuclease (MNase) enzyme to digest chromatin prior to proximity ligation, rather than employing restriction enzymes for fragmentation like 3C technologies. This additional digestion step is designed to investigate proximity between pairs of nucleosomes; cutting the cross-linked genome with MNase yields mononucleosomes, from which genome structure can be mapped at nucleosome resolution. The resolution of Micro-C thus lies between the base-pair resolution of ChIP-Seq methods and that of 3C methods, which cannot capture structures smaller than roughly 1 Kb (de Souza, 2015).

Though the two technologies perform roughly equivalently in their capture of long-range interactions, like hierarchical structural chromosome features, Micro-C produces a significantly improved signal-to-noise ratio compared to Hi-C in its detection of close-range interactions. Additionally, Micro-C's employs single-ended analysis, rather than explicitly considering genome pairs; this allows for the genome-wide mapping of nucleosome occupancy, which can be used to study how chromatin accessibility is linked to the structural features present (Burgess, 2020).

| ![](https://lh3.googleusercontent.com/_uL3pKUSUyqQAbx8WLrSCkiBaIIXXitv7DUGEIZwTJ9zNTa1SGthqszkXlRf393uJI7IDTov7S819xonuiOC-ddLMiRmbyYO9Hwf0zr54kHseaGEsxTrt4mAXRK7KUyNgdwQYeIbi9eMQ0-jU4FKZ5puFSxk-etuF29UUgEwBA94BUdoifXyA48mIIPOoA)|
|:--:|
|Micro-C is advantageous over Hi-C when it comes to coverage resolution, such as in the accurate detection of nucleosome-free regions (NFRs).
(Dovetail Genomics, n.d.)|


#### ChIA-PET

ChIA-PET (Chromatin Interaction Analysis with Paired-End Tag) sequencing is an emerging technology that integrates elements from ChIP-based methods and 3C methods, to leverage the advantages of both.

For context on both kinds of methods, ChIP-based methods can be used to identify transcription factor (TF) binding sites on a genome-wide scale, but cannot be used to determine the interactions between the protein binding sites or the target genes for distal TF binding sites. On the other hand, 3C-family methods and derivatives can reveal long-range chromatin interactions involved in transcription regulation, but are limited by low-throughput and cannot be used to map the entire genome in high resolution. Additionally, both ChIP-Seq and 3C methods suffer from high background noise, resulting from the detection of false positives; the noise increases with greater distance between the interacting regions being examined (Li et al., 2014).

In the workflow for ChiA-PET, the DNA-protein complexes in the sample are first crosslinked with formaldehyde and fragmented via sonication, to reduce non-specific interactions and break up chromatin. This is followed by an immunoprecipitation step, similar to the one used in Hi-C to map long-range DNA interactions, where selected antibodies are used to immunoprecipitate proteins of interest. Next, linkers are ligated to the DNA fragment ends; these two linkers are distinct from each other, distinguished by two different nucleotide barcodes, and thus separate the sample into separate aliquots. They then continue to self-ligate, based on proximity. Finally, the DNA aliquots are precipitated, digested with restriction enzymes, and sequenced.

Both ChIA-PET and Hi-C analyses produce 3D genome-wide capture. Compared to Hi-C, ChIA-PET greatly enhances the resolution, though it is limited to identifying interactions mediated by a known protein, whereas Hi-C can capture all interactions. Additionally, the sonication step in ChIA-PET reduces the non-specific noise found in ChIP-Seq, and the immunoprecipitation step reduces data complexity, often leading to easier data analysis than Hi-C. The main drawbacks of ChIA-PET are its limited sensitivity, potentially ambiguous DNA interactions due to the linkers' self-ligation, and the large amount of starting material required by the method [(Illumina, n.d)](https://www.zotero.org/google-docs/?XofpSS).


| ![](https://lh4.googleusercontent.com/o_APB_F3zLIbSDHpENcJnWIbHtZPowT2xtsgSeZvgmg8uPfL6KhW3wMIJcEOIAN_O7d7k-4X36zl7TcCMrvB_v3jWmsg5qOQpI8DcHal2dPcxPPg_9GirewdcF_til83--4jT6A14Dx69TT7bXoQTTvlwttUE0qdHzLd6bdOBH_iQwnS_cmC001DwppVIw) |
|:--:|
|ChIA-PET workflow
(Li et al., 2019)|


### Other Technologies
------------------

There exist other technologies that don't rely on proximity ligation of pieces. Most of these are both very novel, and not in widespread use. They are however extremely useful for detecting multi-interacting loci, and therefore offer a unique perspective on the structure of the 3D genome.

#### GAM

Genome Architecture Mapping (GAM) is a novel method for discovering 3D contacts. This process, unlike the others, relies on cryosectioning and microdissection. Nuclei are sliced into ultrathin cryosections. They are then laser microdissected, to isolate individual slices. This is particularly advantageous as it eliminates biases that may come from cell extraction and sorting. The main advantage is the ability to detect contacts between multiple loci, and to do this with a low cell number. Indeed with only a small number of slices, a resolution of 30Kb is achievable, given the same amount of sequencing depth as a standard HiC library. [(Kempfer & Pombo, 2020)](https://www.zotero.org/google-docs/?TpfPNI). GAM however requires the use of specialized statistical models called SLICE (Statistical Inference of cosegregation). This isn't necessarily advantageous, as further developments on this have less previous modeling to work on, and users may be unfamiliar with the peculiarities of the modeling and analysis. [(Beagrie et al., 2017)](https://www.zotero.org/google-docs/?in0lAx)

#### SPRITE

| ![](https://lh4.googleusercontent.com/mRcDUMFFcIjcLGv7XWOkpDhHaHq6wVISSGmWYMZhpw-6zIv3er3HRmrpkmtAsbKEVC9xiru0Wm7ayaqNIbdqM3Jvnt8Rjy3dQiCZWPoeKN-avW-nzU5a0Ugoo_8LRP4srrkekFt3RChPXFD3_lQKzsOaUMPdorzw9V4miPaFW-jFU5FjiVQ1DflOY8IXXg)|
|:--:|
|SPRITE workflow schematic
[(Quinodoz et al., 2018)](https://www.zotero.org/google-docs/?JYEHsY)|

SPRITE (Split-Pool Recognition of Interactions by Tag Extension) is another non ligation based method to map complex genome contacts. Like GAM, it also does not rely on ligation. However, SPRITE takes an extremely different approach. Specifically, the sample is crosslinked. Then the sample is split into a 96 well plate. Each well on the plate is assigned a tag. Then the sample is pooled, and this process is repeated multiple times. The end result is that regions associated together in 3D space will always be in the same plate, since they are crosslinked. Therefore they will have a unique sequence of tags assigned to them.[(Quinodoz et al., 2022)](https://www.zotero.org/google-docs/?T1h8Z3) The main advantage of SPRITE over 3C based methods is the ability to detect loci that have multiple interactors. Additionally, SPRITE can also detect RNA-DNA contacts, something GAM has not been used for. In addition, SPRITE can also be combined with immunoprecipitation to see interactions mediated by specific proteins. One disadvantage it shares with GAM is the requirement for specific software tools that aren't commonly used, leading to user difficulty. An advantage it has over GAM is that the sample preparation is much less technically complex than that in GAM.[(Quinodoz et al., 2018)](https://www.zotero.org/google-docs/?B6RoGC)

### Directions for Future Development
---------------------------------

HiC has traditionally been limited by large restriction fragments, which limit the resolution of the data. However,recent steps have been made to improve on this. Indeed, Micro-C in and of itself was a large step towards higher resolution based data. However, other steps have been made that further improve on Micro-C approaches, such as Micro-Capture-C, which allow sub-kilobase resolutions [(Hua et al., 2021)](https://www.zotero.org/google-docs/?Cj1OiP). However these methods aren't applicable genome wide, and must be targeted to a particular region. Therefore, an important next step in chromosome capture is the improvement of genome wide resolution maps. These are particularly important for global mappings of enhancer-promoter contacts, which are usually very small regions that can not be visualized by HiC. Additionally, HiC requires deep sequencing, and is very costly to perform. This is a major barrier to its widespread use in research. Improvements on HiC cost could help revolutionize our understanding of diseases such as cancer, where epigenetic restructuring is one of the drivers of disease. 
 
