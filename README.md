## Strand_seq_practical_computational, Day 6 - Friday 17 May 2019
In this practical session, we will align the raw data to genome and make chromosome plot using Strand-seq data
You can download the example data using the following command lines

## RPE1 C7 data
wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20301_1_sequence.txt.gz https://www.dropbox.com/s/kayg7n0l7mm88wq/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20301_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20301_2_sequence.txt.gz https://www.dropbox.com/s/pit8jt3858z5ug2/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20301_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20302_1_sequence.txt.gz https://www.dropbox.com/s/na4mgn0fb0dyaow/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20302_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20302_2_sequence.txt.gz https://www.dropbox.com/s/fz4u9vxzbbpy3pl/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20302_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20303_1_sequence.txt.gz https://www.dropbox.com/s/tk2oogu5lx6dtyv/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20303_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20303_2_sequence.txt.gz https://www.dropbox.com/s/hzk6qfnxax947h4/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20303_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20304_1_sequence.txt.gz https://www.dropbox.com/s/pj2ld65cmrlzgde/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20304_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20304_2_sequence.txt.gz https://www.dropbox.com/s/59slxjvq2bgd4ws/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20304_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20305_1_sequence.txt.gz https://www.dropbox.com/s/xnwu6u9gpejecaf/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20305_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20305_2_sequence.txt.gz https://www.dropbox.com/s/fgi5xvcer9oco0y/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20305_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20306_1_sequence.txt.gz https://www.dropbox.com/s/92qbxcn0mcco4ec/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20306_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20306_2_sequence.txt.gz https://www.dropbox.com/s/ckg83giw8jkc96o/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20306_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20307_1_sequence.txt.gz https://www.dropbox.com/s/17h8rcxoqwk8lu5/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20307_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20307_2_sequence.txt.gz https://www.dropbox.com/s/tjuo1kyrydhh8zg/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20307_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20308_1_sequence.txt.gz https://www.dropbox.com/s/q94h753wotunsl1/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20308_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20308_2_sequence.txt.gz https://www.dropbox.com/s/4y0drj8zggfqejt/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20308_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20309_1_sequence.txt.gz https://www.dropbox.com/s/fhc72leb9sbdi7k/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20309_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20309_2_sequence.txt.gz https://www.dropbox.com/s/zbdjwwvuwph4gio/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20309_2_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20310_1_sequence.txt.gz https://www.dropbox.com/s/u04ux2pn8tbhuh7/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20310_1_sequence.txt.gz?dl=0

wget -O H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20310_2_sequence.txt.gz https://www.dropbox.com/s/46cv4wu0ioo79ol/H2KT2AFXY_C7x02_18s002199-1-1_Raeder_lane1C7x02PE20310_2_sequence.txt.gz?dl=0

