[##<ins> **Non-native-conformation-generation-by-threading**</ins>](https://github.com/ABLab2018/Codes_with_Python_Layer/tree/main/threading-conformation-generation)

**Step 1**: Extract Calpha coordinates of the target proteins using coord-ext-CA-pro.ipynb

**Step 2**: Get the Calpha coordinates of all proteins taken for non-native conformation generation using threading-conf-gen.ipynb

**Step 3**: Combine extracted Calpha coordinates of targets with the Calpha coordinates of generated non-native conformations (two targets, two such files)

**Step 4**: Convert each protein coordinates them into individual pdb files to calculate RMSD with target using pdb.ipynb

**Step 5**: Calculate Contact profile for both using contact-profile.ipynb (Here, showing for only 2LHC)

**Step 6**: calculate nearest 10 Calpha distances for each site in each protein using calculate-CA-distance.ipynb (Do this for both targets

**Step 7**: Bin the calculated Calpha distances into distinct bins (here bin size =0.2) (Do this for both targets)

[##<ins> **One-body-potential**</ins>](https://github.com/ABLab2018/Codes_with_Python_Layer/tree/main/one-body-potential)

**Step 1**: Calculate Calpha distances between nearest 10 amino acids using cal-dist-between-aa-for-pot-gen.ipynb. Showing for only ALA, repeat this for all remaining 19 amino acids.

**Step 2**: Move all output files into a folder Convert the distances into distinct bins. 

**Step 3**: After this extract each nearest neighbour distances of all amino acids into single file using extract-nn-distance-into-single-file.ipynb

**Step 4**: Calculate average using cal-prob-based-on-bin-size.ipynb

**Step 5**: Calculate potential using pot-gen-modified.ipynb and replace "Nan" and "Infinity" values in the resulting files by the highest potential value using all-pot-replace-infinity.ipynb.

**Step 6**: Finally, combine all potential files into one file using extract-all-pot-into-1-file.ipynb.

[##<ins> **Two-body-potential**</ins>](https://github.com/ABLab2018/Codes_with_Python_Layer/tree/main/two-body-potential)
**Step 1**:Calculate two body contacts using all-contact-and-actual-contact.ipynb ( here shown for cut off range 0-5 )

**Step 2**: Calculate individual probabilites using individual-probability-all-aminoacids.ipynb

**Step 3**: Calculate actual pair probability using actual-pair-prob.ipynb

**Step 4**: Then run multi-individual-prob.ipynb

**Step 5**: Then run multi-indi-prob-and-actual-pair-prob.ipynb

**Step 6** Finally run two-body-potential-modified.ipynb

[##<ins> **Protein-sequence-design**</ins>](https://github.com/ABLab2018/Codes_with_Python_Layer/tree/main/sequence-design)

**Step 1** :Required inputs: One body potential file, two body potential files, contact profiles, bin indexes for all C-alpha distances for all nearest neighbours, input sequences

**Step 2** :Run mc-foldswitch.ipynb
