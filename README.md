# Phylogenomic Interrogation of Ursidae

![NGMI_Panda](Images/Surprised.png)
"Wow, we don't know how bears are related? We're definitely NGMI..."

## Pre-Note
This GitHub repo is a walkthrough of a phylogenomics exploration of the publicly available sequence data for bears [Ursidae]. For evolutionary context, this analysis also includes a few members from the other Caniformia families.

## Datasets
| SRR         | Species                         | Group       | Status  | SISRS_ID           | Raw_Bases       | Trim_Bases      | Percent_Surviving |
|-------------|---------------------------------|-------------|---------|--------------------|-----------------|-----------------|-------------------|
| SRR2712398  | Ailurus fulgens                 | Ailuridae   | Extant  | AilFul_SRR2712398  | 34,124,425,400  | 33,080,299,251  | 96.9%             |
| SRR10425127 | Ailuropoda melanoleuca          | Ursidae     | Extant  | AilMel_SRR10425127 | 32,177,160,000  | 30,197,972,375  | 93.8%             |
| SRR10426210 | Ailuropoda melanoleuca          | Ursidae     | Extant  | AilMel_SRR10426210 | 30,798,799,254  | 28,512,392,089  | 92.6%             |
| SRR504890   | Ailuropoda melanoleuca          | Ursidae     | Extant  | AilMel_SRR504890   | 17,150,021,600  | 14,236,797,948  | 83.0%             |
| SRR2658571  | Arctocephalus gazella           | Otariidae   | Extant  | ArcGaz_SRR2658571  | 41,388,389,232  | 38,218,917,803  | 92.3%             |
| ERR6016610  | Arctodus simus                  | Ursidae     | Extinct | ArcSim_ERR6016610  | 3,236,703,066   | 465,482,695     | 14.4%             |
| ERR6016611  | Arctodus simus                  | Ursidae     | Extinct | ArcSim_ERR6016611  | 56,489,240,767  | 32,752,524,569  | 58.0%             |
| SRR11097187 | Bassariscus sumichrasti         | Procyonidae | Extant  | BasSum_SRR11097187 | 150,573,608,616 | 148,015,035,249 | 98.3%             |
| ERR4317933  | Canis lupus                     | Canidae     | Extant  | CanLup_ERR4317933  | 40,156,489,416  | 39,694,376,165  | 98.8%             |
| SRR6433052  | Eumetopias jubatus              | Otariidae   | Extant  | EumJub_SRR6433052  | 42,059,223,202  | 41,736,091,472  | 99.2%             |
| ERR1007379  | Gulo gulo                       | Mustelidae  | Extant  | GulGul_ERR1007379  | 46,873,725,800  | 41,571,145,810  | 88.7%             |
| SRR11537151 | Halichoerus grypus              | Phocidae    | Extant  | HalGry_SRR11537151 | 18,845,015,628  | 16,309,464,553  | 86.5%             |
| ERR946784   | Helarctos malayanus             | Ursidae     | Extant  | HelMal_ERR946784   | 27,097,378,920  | 25,522,922,974  | 94.2%             |
| ERR946785   | Helarctos malayanus             | Ursidae     | Extant  | HelMal_ERR946785   | 29,574,784,440  | 27,805,245,166  | 94.0%             |
| SRR13167983 | Helarctos malayanus             | Ursidae     | Extant  | HelMal_SRR13167983 | 155,068,385,752 | 152,135,172,077 | 98.1%             |
| SRR14298102 | Leptonychotes weddellii         | Phocidae    | Extant  | LepWed_SRR14298102 | 38,126,054,326  | 36,378,610,039  | 95.4%             |
| ERR3316172  | Lutra lutra                     | Mustelidae  | Extant  | LutLut_ERR3316172  | 38,126,117,444  | 34,860,625,817  | 91.4%             |
| SRR7759803  | Lycaon pictus                   | Canidae     | Extant  | LycPic_SRR7759803  | 38,688,607,200  | 35,114,228,095  | 90.8%             |
| ERR946786   | Melursus ursinus                | Ursidae     | Extant  | MelUrs_ERR946786   | 27,150,401,700  | 25,565,216,026  | 94.2%             |
| ERR1697189  | Neovison vison                  | Mustelidae  | Extant  | NeoVis_ERR1697189  | 38,728,033,200  | 36,430,764,071  | 94.1%             |
| SRR575511   | Odobenus rosmarus divergens     | Odobenidae  | Extant  | OdoRos_SRR575511   | 33,732,365,416  | 31,756,137,457  | 94.1%             |
| SRR10340436 | Phocarctos hookeri              | Otariidae   | Extant  | PhoHoo_SRR10340436 | 52,184,479,580  | 50,691,443,108  | 97.1%             |
| SRR11679518 | Phoca vitulina                  | Phocidae    | Extant  | PhoVit_SRR11679518 | 16,380,628,282  | 14,577,790,499  | 89.0%             |
| SRR11248589 | Potos flavus                    | Procyonidae | Extant  | PotFla_SRR11248589 | 45,669,665,506  | 41,314,368,505  | 90.5%             |
| SRR11268446 | Procyon lotor                   | Procyonidae | Extant  | ProLot_SRR11268446 | 41,395,283,290  | 34,327,425,993  | 82.9%             |
| SRR7704832  | Spilogale gracilis              | Mephitidae  | Extant  | SpiGra_SRR7704832  | 77,409,354,302  | 76,942,242,949  | 99.4%             |
| ERR946788   | Tremarctos ornatus              | Ursidae     | Extant  | TreOrn_ERR946788   | 29,284,343,100  | 27,538,255,171  | 94.0%             |
| SRR13602719 | Tremarctos ornatus              | Ursidae     | Extant  | TreOrn_SRR13602719 | 173,848,373,222 | 168,334,933,159 | 96.8%             |
| SRR16086837 | Tremarctos ornatus              | Ursidae     | Extant  | TreOrn_SRR16086837 | 200,433,191,026 | 195,287,163,678 | 97.4%             |
| SRR5198003  | Urocyon littoralis              | Canidae     | Extant  | UroLit_SRR5198003  | 39,569,458,800  | 34,678,809,480  | 87.6%             |
| SRR518723   | Ursus americanus                | Ursidae     | Extant  | UrsAme_SRR518723   | 90,075,056,240  | 75,653,846,070  | 84.0%             |
| SRR7813602  | Ursus americanus                | Ursidae     | Extant  | UrsAme_SRR7813602  | 83,879,492,250  | 83,318,589,119  | 99.3%             |
| SRR830685   | Ursus americanus                | Ursidae     | Extant  | UrsAme_SRR830685   | 51,037,103,100  | 43,269,939,659  | 84.8%             |
| ERR2678639  | Ursus arctos                    | Ursidae     | Extant  | UrsArc_ERR2678639  | 64,391,843,248  | 51,538,769,514  | 80.0%             |
| SRR518710   | Ursus arctos                    | Ursidae     | Extant  | UrsArc_SRR518710   | 80,724,351,000  | 74,149,015,165  | 91.9%             |
| SRR830213   | Ursus arctos                    | Ursidae     | Extant  | UrsArc_SRR830213   | 54,730,458,900  | 46,073,915,458  | 84.2%             |
| ERR2678617  | Ursus ingressus                 | Ursidae     | Extinct | UrsIng_ERR2678617  | 61,348,745,320  | 16,830,949,317  | 27.4%             |
| ERR5032144  | Ursus ingressus                 | Ursidae     | Extinct | UrsIng_ERR5032144  | 32,590,754,568  | 9,845,698,814   | 30.2%             |
| ERR5084685  | Ursus ingressus                 | Ursidae     | Extinct | UrsIng_ERR5084685  | 19,337,892,960  | 7,007,268,607   | 36.2%             |
| ERR5084686  | Ursus ingressus                 | Ursidae     | Extinct | UrsIng_ERR5084686  | 17,951,024,668  | 6,407,201,431   | 35.7%             |
| ERR5084798  | Ursus ingressus                 | Ursidae     | Extinct | UrsIng_ERR5084798  | 8,991,374,538   | 4,630,292,643   | 51.5%             |
| ERR2678626  | Ursus kudarensis                | Ursidae     | Extinct | UrsKud_ERR2678626  | 36,240,161,936  | 11,354,157,196  | 31.3%             |
| ERR5084693  | Ursus kudarensis praekudarensis | Ursidae     | Extinct | UrsKud_ERR5084693  | 29,854,468,732  | 6,110,981,162   | 20.5%             |
| ERR5084743  | Ursus kudarensis praekudarensis | Ursidae     | Extinct | UrsKud_ERR5084743  | 65,007,995,728  | 7,467,145,470   | 11.5%             |
| ERR5084744  | Ursus kudarensis praekudarensis | Ursidae     | Extinct | UrsKud_ERR5084744  | 58,726,615,584  | 7,162,860,983   | 12.2%             |
| ERR5084752  | Ursus kudarensis                | Ursidae     | Extinct | UrsKud_ERR5084752  | 123,239,944,070 | 20,083,823,914  | 16.3%             |
| SRR518682   | Ursus maritimus                 | Ursidae     | Extant  | UrsMar_SRR518682   | 84,271,335,862  | 77,803,810,108  | 92.3%             |
| SRR942294   | Ursus maritimus                 | Ursidae     | Extant  | UrsMar_SRR942294   | 40,925,140,000  | 38,085,791,074  | 93.1%             |
| SRR942296   | Ursus maritimus                 | Ursidae     | Extant  | UrsMar_SRR942296   | 40,122,522,000  | 35,313,777,171  | 88.0%             |
| ERR5084688  | Ursus rossicus                  | Ursidae     | Extinct | UrsRos_ERR5084688  | 17,416,613,948  | 3,724,537,100   | 21.4%             |
| ERR5084689  | Ursus rossicus                  | Ursidae     | Extinct | UrsRos_ERR5084689  | 26,221,669,796  | 5,635,707,253   | 21.5%             |
| ERR2678615  | Ursus spelaeus eremus           | Ursidae     | Extinct | UrsSpe_ERR2678615  | 75,154,681,032  | 13,070,797,668  | 17.4%             |
| ERR2678619  | Ursus spelaeus                  | Ursidae     | Extinct | UrsSpe_ERR2678619  | 59,987,397,450  | 8,041,974,053   | 13.4%             |
| ERR946787   | Ursus thibetanus                | Ursidae     | Extant  | UrsThi_ERR946787   | 30,504,678,120  | 28,513,030,996  | 93.5%             |
| SRR10233895 | Ursus thibetanus thibetanus     | Ursidae     | Extant  | UrsThi_SRR10233895 | 14,200,815,300  | 13,029,443,666  | 91.8%             |
| SRR8206115  | Ursus thibetanus ussuricus      | Ursidae     | Extant  | UrsThi_SRR8206115  | 44,635,093,546  | 43,416,567,248  | 97.3%             |