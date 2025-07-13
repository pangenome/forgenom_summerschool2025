# PhD School on Modern Bioinformatics towards Pangenomics

Summer School & Hackathon \
July 8-14 2025, Ischia, Italy \
https://algolab.github.io/forgenom_summerschool2025/

## Compressing and accelerating exabytes of pangenomic data

**Presentation**: https://docs.google.com/presentation/d/1h0-KhrZk03BNiQogRZiy685fUu2NEVR8Zf0NJnTiCCM/edit?usp=sharing

### GBAM hacking ideas
- Can we use AGC (Assembled Genomes Compressor) for read sequencing compression? If yes, start integrating it in GBAM.
- Search the literature for ad hoc solutions for sequencing data compression, benchmark some of them, and start integrating the winners in GBAM.
- Compress metadata

### IMPG hacking ideas
- Can we have a compressed IMPG index? If yes, implement it in IMPG.
- Compare graphs built with PGGB vs "IMPG partition + PGGBs/AlfaPang/POAs + GFALACE" in terms of graph statistics (graph lengths, # nodes, # edges, # steps), panacus statistics, variants called.
- Can we remove entries from the input alignments without losing too much (transitive) connectivity? Potential new `impg reduce` command.
- Improve how GFALACE manages overlaps between subgraphs: now it just trims one of them. A better way would be to take sequences that overlap, POA, get the POA-graph and lace it to resolve the overlap.
