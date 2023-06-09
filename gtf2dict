def gtf2dict(gtfFile):
    geneDict = {}
    with open(gtfFile,"r") as gtf:
        for line in gtf:
            if line.startswith("#") == False:
                data = line.split("\t")
                if data[2] == "gene" and 'gene_biotype "protein_coding"' in data[-1]:
                    id = data[-1].split("gene_id ")[1].replace('"','').split(";")[0]
                    chr = data[0]
                    c1 = int(data[3])
                    c2 = int(data[4])
                    strand = data[6]
                    geneDict[id] = {"chr":chr, "c1":c1, "c2":c2, "strand":strand}
    return geneDict
