kill %1

conda activate drug-repurposing
cd /home/chemthings/Drug_Repurposing

drug-repurposing run \
  --condition "rheumatoid arthritis" \
  --select MONDO_0008383 \
  --ligands data/ligands/Drugs_Chembl.cleaned.csv \
  --gnina-path /home/chemthings/gnina-1.3.3-build-dock/bin/gnina \
  --output outputs/ra_chembl_full \
  --config examples/config.yaml
