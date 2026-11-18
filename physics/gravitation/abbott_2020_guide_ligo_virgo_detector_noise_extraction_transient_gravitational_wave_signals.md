Source: see manifest row of the PDF
PDF sha256: d62eeff5e2917e091a0ea53acbad757f0ae41e6cebaef8ac04b501c979184093
License: CC-BY
Language: eng
Fidelity: machine-gated

# Transcription of abbott_2020_guide_ligo_virgo_detector_noise_extraction_transient_gravitational_wave_signals.pdf

Transcription of `abbott_2020_guide_ligo_virgo_detector_noise_extraction_transient_gravitational_wave_signals.pdf` in this directory, 55 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-55 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

UvA-DARE (Digital Academic Repository)

A guide to LIGO-Virgo detector noise and extraction of transient gravitationalwave signals
Abbott, B.P.; Caudill, S.; Ghosh, A.; Hinderer, T.; Linde, F.; Nichols, D.; Nissanke, S.; Phukon,
K.S.; van Bakel, N.; van Beuzekom, M.; Vardaro, M.; Williamson, A.R.; The LIGO Scientific
Collaboration; Virgo Collaboration
DOI
10.1088/1361-6382/ab685e
Publication date
2020
Document Version
Final published version
Published in
Classical and Quantum Gravity
License
CC BY
Link to publication
Citation for published version (APA):
Abbott, B. P., Caudill, S., Ghosh, A., Hinderer, T., Linde, F., Nichols, D., Nissanke, S.,
Phukon, K. S., van Bakel, N., van Beuzekom, M., Vardaro, M., Williamson, A. R., The LIGO
Scientific Collaboration, & Virgo Collaboration (2020). A guide to LIGO-Virgo detector noise
and extraction of transient gravitational-wave signals. Classical and Quantum Gravity, 37(5),
[055002]. https://doi.org/10.1088/1361-6382/ab685e

General rights
It is not permitted to download or to forward/distribute the text or part of it without the consent of the author(s)
and/or copyright holder(s), other than for strictly personal, individual use, unless the work is under an open
content license (like Creative Commons).
Disclaimer/Complaints regulations
If you believe that digital publication of certain material infringes any of your rights or (privacy) interests, please
let the Library know, stating your reasons. In case of a legitimate complaint, the Library will make the material
inaccessible and/or remove it from the website. Please Ask the Library: https://uba.uva.nl/en/contact, or a letter
to: Library of the University of Amsterdam, Secretariat, Singel 425, 1012 WP Amsterdam, The Netherlands. You
UvA-DARE is a service provided by the library of the University of Amsterdam (https://dare.uva.nl)
will be contacted as soon as possible.
Download date:27 Aug 2022

## PDF page 2

Classical and Quantum Gravity
Class. Quantum Grav. 37 (2020) 055002 (54pp)

https://doi.org/10.1088/1361-6382/ab685e

A guide to LIGO–Virgo detector noise and
extraction of transient gravitational-wave
signals
B P Abbott1, R Abbott1, T D Abbott2, S Abraham3,
F Acernese4,5, K Ackley6, C Adams7, V B Adya8,9, C Affeldt8,9,
M Agathos10, K Agatsuma11, N Aggarwal12, O D Aguiar13,
L Aiello14,15, A Ain3, P Ajith16, T Alford1, G Allen17,
A Allocca18,19, M A Aloy20, P A Altin21, A Amato22,
A Ananyeva1, S B Anderson1, W G Anderson23,
S V Angelova24, S Antier25, S Appert1, K Arai1, M C Araya1,
J S Areeda26, M Arène27, N Arnaud25,28, K G Arun29,
S Ascenzi30,31, G Ashton6, S M Aston7, P Astone32, F Aubin33,
P Aufmuth9, K AultONeal34, C Austin2, V Avendano35,
A Avila-Alvarez26, S Babak27,36, P Bacon27, F Badaracco14,15,
M K M Bader37, S Bae38, P T Baker39, F Baldaccini40,41,
G Ballardin28, S W Ballmer42, S Banagiri43, J C Barayoga1,
S E Barclay44, B C Barish1, D Barker45, K Barkett46,
S Barnum12, F Barone4,5, B Barr44, L Barsotti12,
M Barsuglia27, D Barta47, J Bartlett45, I Bartos48, R Bassiri49,
A Basti18,19, M Bawaj41,50, J C Bayley44, M Bazzan51,52,
B Bécsy53, M Bejger27,54, I Belahcene25, A S Bell44,
D Beniwal55, B K Berger49, G Bergmann8,9, S Bernuzzi56,57,
J J Bero58, C P L Berry59, D Bersanetti60, A Bertolini37,
J Betzwieser7, R Bhandare61, J Bidler26, I A Bilenko62,
S A Bilgili39, G Billingsley1, J Birch7, R Birney24,
O Birnholtz58, S Biscans1,12, S Biscoveanu6, A Bisht9,
M Bitossi19,28, M A Bizouard25, J K Blackburn1, C D Blair7,
D G Blair63, R M Blair45, S Bloemen64, N Bode8,9, M Boer65,
Y Boetzel66, G Bogaert65, F Bondu67, E Bonilla49,
R Bonnand33, P Booker8,9, B A Boom37, C D Booth68,
R Bork1, V Boschi28, S Bose3,69, K Bossie7, V Bossilkov63,
J Bosveld63, Y Bouffanais27, A Bozzi28, C Bradaschia19,
P R Brady23, A Bramley7, M Branchesi14,15, J E Brau70,
T Briant71, J H Briggs44, F Brighenti72,73, A Brillet65,
M Brinkmann8,9, V Brisson25,177, P Brockill23, A F Brooks1,
Original content from this work may be used under the terms of the Creative
Commons Attribution 4.0 licence. Any further distribution of this work must maintain
attribution to the author(s) and the title of the work, journal citation and DOI.
1361-6382/20/055002+54$33.00 © 2020 IOP Publishing Ltd Printed in the UK

1

## PDF page 3

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

D D Brown55, S Brunett1, A Buikema12, T Bulik74,
H J Bulten37,75, A Buonanno36,76, D Buskulic33, C Buy27,
R L Byer49, M Cabero8,9, L Cadonati77, G Cagnoli22,78,
C Cahillane1, J Calderón Bustillo6, T A Callister1,
E Calloni5,79, J B Camp80, W A Campbell6, M Canepa60,81,
K C Cannon82, H Cao55, J Cao83, E Capocasa27,
F Carbognani28, S Caride84, M F Carney59, G Carullo18,
J Casanueva Diaz19, C Casentini30,31, S Caudill37,
M Cavaglià85, F Cavalier25, R Cavalieri28, G Cella19,
P Cerdá-Durán20, G Cerretani18,19, E Cesarini31,86, O Chaibi65,
K Chakravarti3, S J Chamberlin87, M Chan44, S Chao88,
P Charlton89, E A Chase59, E Chassande-Mottin27,
D Chatterjee23, M Chaturvedi61, K Chatziioannou90,
B D Cheeseboro39, H Y Chen91, X Chen63, Y Chen46,
H-P Cheng48, C K Cheong92, H Y Chia48, A Chincarini60,
A Chiummo28, G Cho93, H S Cho94, M Cho76,
N Christensen65,95, Q Chu63, S Chua71, K W Chung92,
S Chung63, G Ciani51,52, A A Ciobanu55, R Ciolfi96,97,
F Cipriano65, A Cirone60,81, F Clara45, J A Clark77,
P Clearwater98, F Cleva65, C Cocchieri85, E Coccia14,15,
P-F Cohadon71, D Cohen25, R Colgan99, M Colleoni100,
C G Collette101, C Collins11, L R Cominsky102,
M Constancio Jr13, L Conti52, S J Cooper11, P Corban7,
T R Corbitt2, I Cordero-Carrión103, K R Corley99, N Cornish53,
A Corsi84, S Cortese28, C A Costa13, R Cotesta36,
M W Coughlin1, S B Coughlin59,68, J-P Coulon65,
S T Countryman99, P Couvares1, P B Covas100, E E Cowan77,
D M Coward63, M J Cowart7, D C Coyne1, R Coyne104,
J D E Creighton23, T D Creighton105, J Cripe2, M Croquette71,
S G Crowder106, T J Cullen2, A Cumming44, L Cunningham44,
E Cuoco28, T Dal Canton80, G Dálya107, S L Danilishin8,9,
S D’Antonio31, K Danzmann8,9, A Dasgupta108, C F Da Silva
Costa48, L E H Datrier44, V Dattilo28, I Dave61, M Davier25,
D Davis42, E J Daw109, D DeBra49, M Deenadayalan3,
J Degallaix22, M De Laurentis5,79, S Deléglise71,
W Del Pozzo18,19, L M DeMarchi59, N Demos12, T Dent8,9,110,
R De Pietri57,111, J Derby26, R De Rosa5,79, C De Rossi22,28,
R DeSalvo112, O de Varona8,9, S Dhurandhar3, M C Díaz105,
T Dietrich37, L Di Fiore5, M Di Giovanni97,113, T Di Girolamo5,79,
A Di Lieto18,19, B Ding101, S Di Pace32,114, I Di Palma32,114,
F Di Renzo18,19, A Dmitriev11, Z Doctor91, F Donovan12,
K L Dooley68,85, S Doravari8,9, I Dorrington68, T P Downes23,
M Drago14,15, J C Driggers45, Z Du83, J-G Ducoin25, P Dupej44,
S E Dwyer45, P J Easter6, T B Edo109, M C Edwards95,
A Effler7, P Ehrens1, J Eichholz1, S S Eikenberry48,
2

## PDF page 4

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

M Eisenmann33, R A Eisenstein12, R C Essick91, H Estelles100,
D Estevez33, Z B Etienne39, T Etzel1, M Evans12, T M Evans7,
V Fafone14,30,31, H Fair42, S Fairhurst68, X Fan83, S Farinon60,
B Farr70, W M Farr11, E J Fauchon-Jones68, M Favata35,
M Fays109, M Fazio115, C Fee116, J Feicht1, M M Fejer49,
F Feng27, A Fernandez-Galiana12, I Ferrante18,19,
E C Ferreira13, T A Ferreira13, F Ferrini28, F Fidecaro18,19,
I Fiori28, D Fiorucci27, M Fishbach91, R P Fisher42,117,
J M Fishner12, M Fitz-Axen43, R Flaminio33,118, M Fletcher44,
E Flynn26, H Fong90, J A Font20,119, P W F Forsyth21,
J-D Fournier65, S Frasca32,114, F Frasconi19, Z Frei107,
A Freise11, R Frey70, V Frey25, P Fritschel12, V V Frolov7,
P Fulda48, M Fyffe7, H A Gabbard44, B U Gadre3,
S M Gaebel11, J R Gair120, L Gammaitoni40, M R Ganija55,
S G Gaonkar3, A Garcia26, C García-Quirós100, F Garufi5,79,
B Gateley45, S Gaudio34, G Gaur121, V Gayathri122,
G Gemme60, E Genin28, A Gennai19, D George17, J George61,
L Gergely123, V Germain33, S Ghonge77, Abhirup Ghosh16,
Archisman Ghosh37, S Ghosh23, B Giacomazzo97,113,
J A Giaime2,7, K D Giardina7, A Giazotto19,178, K Gill34,
G Giordano4,5, L Glover112, P Godwin87, E Goetz45, R Goetz48,
B Goncharov6, G González2, J M Gonzalez Castro18,19,
A Gopakumar124, M L Gorodetsky62, S E Gossan1,
M Gosselin28, R Gouaty33, A Grado5,125, C Graef44,
M Granata22, A Grant44, S Gras12, P Grassia1, C Gray45,
R Gray44, G Greco72,73, A C Green11,48, R Green68,
E M Gretarsson34, P Groot64, H Grote68, S Grunewald36,
P Gruning25, G M Guidi72,73, H K Gulati108, Y Guo37, A Gupta87,
M K Gupta108, E K Gustafson1, R Gustafson126, L Haegel100,
O Halim14,15, B R Hall69, E D Hall12, E Z Hamilton68,
G Hammond44, M Haney66, M M Hanke8,9, J Hanks45,
C Hanna87, M D Hannam68, O A Hannuksela92, J Hanson7,
T Hardwick2, K Haris16, J Harms14,15, G M Harry127,
I W Harry36, C-J Haster90, K Haughian44, F J Hayes44,
J Healy58, A Heidmann71, M C Heintze7, H Heitmann65,
P Hello25, G Hemming28, M Hendry44, I S Heng44, J Hennig8,9,
A W Heptonstall1, Francisco Hernandez Vivanco6,
M Heurs8,9, S Hild44, T Hinderer37,128,129, D Hoak28,
S Hochheim8,9, D Hofman22, A M Holgado17, N A Holland21,
K Holt7, D E Holz91, P Hopkins68, C Horst23, J Hough44,
E J Howell63, C G Hoy68, A Hreibi65, E A Huerta17, D Huet25,
B Hughey34, M Hulko1, S Husa100, S H Huttner44,
T Huynh-Dinh7, B Idzkowski74, A Iess30,31, C Ingram55,
R Inta84, G Intini32,114, B Irwin116, H N Isa44, J-M Isac71, M Isi1,
B R Iyer16, K Izumi45, T Jacqmin71, S J Jadhav130, K Jani77,
3

## PDF page 5

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

N N Janthalur130, P Jaranowski131, A C Jenkins132, J Jiang48,
D S Johnson17, A W Jones11, D I Jones133, R Jones44,
R J G Jonker37, L Ju63, J Junker8,9, C V Kalaghatgi68,
V Kalogera59, B Kamai1, S Kandhasamy85, G Kang38,
J B Kanner1, S J Kapadia23, S Karki70, K S Karvinen8,9,
R Kashyap16, M Kasprzack1, S Katsanevas28,
E Katsavounidis12, W Katzman7, S Kaufer9, K Kawabe45,
N V Keerthana3, F Kéfélian65, D Keitel44, R Kennedy109,
J S Key134, F Y Khalili62, H Khan26, I Khan14,31, S Khan8,9,
Z Khan108, E A Khazanov135, M Khursheed61, N Kijbunchoo21,
A X Kim59, Chunglee Kim136, J C Kim137, K Kim92, W Kim55,
W S Kim138, Y-M Kim139, C Kimball59, E J King55, P J King45,
M Kinley-Hanlon127, R Kirchhoff8,9, J S Kissel45,
L Kleybolte140, J H Klika23, S Klimenko48, T D Knowles39,
P Koch8,9, S M Koehlenbeck8,9, G Koekoek37,141, S Koley37,
V Kondrashov1, A Kontos12, N Koper8,9, M Korobko140,
W Z Korth1, I Kowalska74, D B Kozak1, V Kringel8,9,
N Krishnendu29, A Królak142,143, G Kuehn8,9, A Kumar130,
P Kumar144, R Kumar108, S Kumar16, L Kuo88, A Kutynia142,
S Kwang23, B D Lackey36, K H Lai92, T L Lam92, M Landry45,
B B Lane12, R N Lang145, J Lange58, B Lantz49, R K Lanza12,
S Larson59, A Lartaux-Vollard25, P D Lasky6, M Laxen7,
A Lazzarini1, C Lazzaro52, P Leaci32,114, S Leavey8,9,
Y K Lecoeuche45, C H Lee94, H K Lee146, H M Lee147,
H W Lee137, J Lee93, K Lee44, J Lehmann8,9, A Lenon39,
N Leroy25, N Letendre33, Y Levin6,99, J Li83, K J L Li92,
T G F Li92, X Li46, F Lin6, F Linde37, S D Linker112,
T B Littenberg148, J Liu63, X Liu23, R K L Lo1,92,
N A Lockerbie24, L T London68, A Longo149,150,
M Lorenzini14,15, V Loriette151, M Lormand7, G Losurdo19,
J D Lough8,9, C O Lousto58, G Lovelace26, M E Lower152,
H Lück9,8, D Lumaca30,31, A P Lundgren153, R Lynch12, Y Ma46,
R Macas68, S Macfoy24, M MacInnis12, D M Macleod68,
A Macquet65, F Magaña-Sandoval42, L Magaña Zertuche85,
R M Magee87, E Majorana32, I Maksimovic151, A Malik61,
N Man65, V Mandic43, V Mangano44, G L Mansell12,45,
M Manske21,23, M Mantovani28, F Marchesoni41,50, F Marion33,
S Márka99, Z Márka99, C Markakis10,17, A S Markosyan49,
A Markowitz1, E Maros1, A Marquina103, S Marsat36,
F Martelli72,73, I W Martin44, R M Martin35, D V Martynov11,
K Mason12, E Massera109, A Masserot33, T J Massinger1,
M Masso-Reid44, S Mastrogiovanni32,114, A Matas36,43,
F Matichard1,12, L Matone99, N Mavalvala12, N Mazumder69,
J J McCann63, R McCarthy45, D E McClelland21,
S McCormick7, L McCuller12, S C McGuire154, J McIver1,
4

## PDF page 6

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

D J McManus21, T McRae21, S T McWilliams39, D Meacher87,
G D Meadors6, M Mehmet8,9, A K Mehta16, J Meidam37,
A Melatos98, G Mendell45, R A Mercer23, L Mereni22,
E L Merilh45, M Merzougui65, S Meshkov1, C Messenger44,
C Messick87, R Metzdorff71, P M Meyers98, H Miao11,
C Michel22, H Middleton98, E E Mikhailov155, L Milano5,79,
A L Miller48, A Miller32,114, M Millhouse53, J C Mills68,
M C Milovich-Goff112, O Minazzoli65,156, Y Minenkov31,
A Mishkin48, C Mishra157, T Mistry109, S Mitra3,
V P Mitrofanov62, G Mitselmakher48, R Mittleman12, G Mo95,
D Moffa116, K Mogushi85, S R P Mohapatra12, M Montani72,73,
C J Moore10, D Moraru45, G Moreno45, S Morisaki82,
B Mours33, C M Mow-Lowry11, Arunava Mukherjee8,9,
D Mukherjee23, S Mukherjee105, N Mukund3, A Mullavey7,
J Munch55, E A Muñiz42, M Muratore34, P G Murray44,
A Nagar86,158,159, I Nardecchia30,31, L Naticchioni32,114,
R K Nayak160, J Neilson112, G Nelemans37,64, T J N Nelson7,
M Nery8,9, A Neunzert126, K Y Ng12, S Ng55, P Nguyen70,
D Nichols37,128, S Nissanke37,128, F Nocera28, C North68,
L K Nuttall153, M Obergaulinger20, J Oberling45,
B D O’Brien48, G D O’Dea112, G H Ogin161, J J Oh138,
S H Oh138, F Ohme8,9, H Ohta82, M A Okada13, M Oliver100,
P Oppermann8,9, Richard J Oram7, B O’Reilly7,
R G Ormiston43, L F Ortega48, R O’Shaughnessy58,
S Ossokine36, D J Ottaway55, H Overmier7, B J Owen84,
A E Pace87, G Pagano18,19, M A Page63, A Pai122, S A Pai61,
J R Palamos70, O Palashov135, C Palomba32, A Pal-Singh140,
Huang-Wei Pan88, B Pang46, P T H Pang92, C Pankow59,
F Pannarale32,114, B C Pant61, F Paoletti19, A Paoli28, A Parida3,
W Parker7,154, D Pascucci44, A Pasqualetti28,
R Passaquieti18,19, D Passuello19, M Patil143, B Patricelli18,19,
B L Pearlstone44, C Pedersen68, M Pedraza1,
R Pedurand22,162, A Pele7, S Penn163, C J Perez45,
A Perreca97,113, H P Pfeiffer36,90, M Phelps8,9, K S Phukon3,
O J Piccinni32,114, M Pichot65, F Piergiovanni72,73, G Pillant28,
L Pinard22, M Pirello45, M Pitkin44, R Poggiani18,19,
D Y T Pong92, S Ponrathnam3, P Popolizio28, E K Porter27,
J Powell152, A K Prajapati108, J Prasad3, K Prasai49,
R Prasanna130, G Pratten100, T Prestegard23, S Privitera36,
G A Prodi97,113, L G Prokhorov62, O Puncken8,9, M Punturo41,
P Puppo32, M Pürrer36, H Qi23, V Quetschke105,
P J Quinonez34, E A Quintero1, R Quitzow-James70,
F J Raab45, H Radkins45, N Radulescu65, P Raffai107, S Raja61,
C Rajan61, B Rajbhandari84, M Rakhmanov105,
K E Ramirez105, A Ramos-Buades100, Javed Rana3, K Rao59,
5

## PDF page 7

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

P Rapagnani32,114, V Raymond68, M Razzano18,19, J Read26,
T Regimbau33, L Rei60, S Reid24, D H Reitze1,48, W Ren17,
F Ricci32,114, C J Richardson34, J W Richardson1,
P M Ricker17, K Riles126, M Rizzo59, N A Robertson1,44,
R Robie44, F Robinet25, A Rocchi31, L Rolland33, J G Rollins1,
V J Roma70, M Romanelli67, R Romano4,5, C L Romel45,
J H Romie7, K Rose116, D Rosińska54,164, S G Rosofsky17,
M P Ross165, S Rowan44, A Rüdiger8,9,179, P Ruggi28,
G Rutins166, K Ryan45, S Sachdev1, T Sadecki45,
M Sakellariadou132, L Salconi28, M Saleem29, A Samajdar37,
L Sammut6, E J Sanchez1, L E Sanchez1, N Sanchis-Gual20,
V Sandberg45, J R Sanders42, K A Santiago35, N Sarin6,
B Sassolas22, B S Sathyaprakash68,87, P R Saulson42,
O Sauter126, R L Savage45, P Schale70, M Scheel46,
J Scheuer59, P Schmidt64, R Schnabel140, R M S Schofield70,
A Schönbeck140, E Schreiber8,9, B W Schulte8,9, B F Schutz68,
S G Schwalbe34, J Scott44, S M Scott21, E Seidel17, D Sellers7,
A S Sengupta167, N Sennett36, D Sentenac28, V Sequino14,30,31,
A Sergeev135, Y Setyawati8,9, D A Shaddock21, T Shaffer45,
M S Shahriar59, M B Shaner112, L Shao36, P Sharma61,
P Shawhan76, H Shen17, R Shink168, D H Shoemaker12,
D M Shoemaker77, S ShyamSundar61, K Siellez77,
M Sieniawska54, D Sigg45, A D Silva13, L P Singer80,
N Singh74, A Singhal14,32, A M Sintes100,
S Sitmukhambetov105, V Skliris68, B J J Slagmolen21,
T J Slaven-Blair63, J R Smith26, R J E Smith6, S Somala169,
E J Son138, B Sorazu44, F Sorrentino60, T Souradeep3,
E Sowell84, A P Spencer44, A K Srivastava108, V Srivastava42,
K Staats59, C Stachie65, M Standke8,9, D A Steer27,
M Steinke8,9, J Steinlechner44,140, S Steinlechner140,
D Steinmeyer8,9, S P Stevenson152, D Stocks49, R Stone105,
D J Stops11, K A Strain44, G Stratta72,73, S E Strigin62,
A Strunk45, R Sturani170, A L Stuver171, V Sudhir12,
T Z Summerscales172, L Sun1, S Sunil108, J Suresh3,
P J Sutton68, B L Swinkels37, M J Szczepańczyk34, M Tacca37,
S C Tait44, C Talbot6, D Talukder70, D B Tanner48, M Tápai123,
A Taracchini36, J D Tasson95, R Taylor1, F Thies8,9,
M Thomas7, P Thomas45, S R Thondapu61, K A Thorne7,
E Thrane6, Shubhanshu Tiwari97,113, Srishti Tiwari124,
V Tiwari68, K Toland44, M Tonelli18,19, Z Tornasi44,
A Torres-Forné173, C I Torrie1, D Töyrä11, F Travasso28,41,
G Traylor7, M C Tringali74, A Trovato27, L Trozzo174,19,
R Trudeau1, K W Tsang37, M Tse12, R Tso46, L Tsukada82,
D Tsuna82, D Tuyenbayev105, K Ueno82, D Ugolini175,
C S Unnikrishnan124, A L Urban2, S A Usman68,
6

## PDF page 8

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

H Vahlbruch9, G Vajente1, G Valdes2, N van Bakel37,
M van Beuzekom37, J F J van den Brand37,75,
C Van Den Broeck37,176, D C Vander-Hyde42,
J V van Heijningen63, L van der Schaaf37, A A van Veggel44,
M Vardaro51,52, V Varma46, S Vass1, M Vasúth47, A Vecchio11,
G Vedovato52, J Veitch44, P J Veitch55, K Venkateswara165,
G Venugopalan1, D Verkindt33, F Vetrano72,73, A Viceré72,73,
A D Viets23, D J Vine166, J-Y Vinet65, S Vitale12, T Vo42,
H Vocca40,41, C Vorvick45, S P Vyatchanin62, A R Wade1,
L E Wade116, M Wade116, R Walet37, M Walker26, L Wallace1,
S Walsh23, G Wang14,19, H Wang11, J Z Wang126, W H Wang105,
Y F Wang92, R L Ward21, Z A Warden34, J Warner45, M Was33,
J Watchi101, B Weaver45, L-W Wei8,9, M Weinert8,9,
A J Weinstein1, R Weiss12, F Wellmann8,9, L Wen63,
E K Wessel17, P Weßels8,9, J W Westhouse34, K Wette21,
J T Whelan58, B F Whiting48, C Whittle12, D M Wilken8,9,
D Williams44, A R Williamson37,128, J L Willis1, B Willke8,9,
M H Wimmer8,9, W Winkler8,9, C C Wipf1, H Wittel8,9,
G Woan44, J Woehler8,9, J K Wofford58, J Worden45,
J L Wright44, D S Wu8,9, D M Wysocki58, L Xiao1,
H Yamamoto1, C C Yancey76, L Yang115, M J Yap21,
M Yazback48, D W Yeeles68, Hang Yu12, Haocun Yu12,
S H R Yuen92, M Yvert33, A K Zadrożny105,142, M Zanolin34,
T Zelenova28, J-P Zendri52, M Zevin59, J Zhang63, L Zhang1,
T Zhang44, C Zhao63, M Zhou59, Z Zhou59, X J Zhu6,
M E Zucker1,12, J Zweizig1 and The LIGO Scientific
Collaboration and the Virgo Collaboration
1

LIGO, California Institute of Technology, Pasadena, CA 91125,
United States of America
2
Louisiana State University, Baton Rouge, LA 70803, United States of America
3
Inter-University Centre for Astronomy and Astrophysics, Pune 411007, India
4
Università di Salerno, Fisciano, I-84084 Salerno, Italy
5
INFN, Sezione di Napoli, Complesso Universitario di Monte S.Angelo, I-80126
Napoli, Italy
6
OzGrav, School of Physics & Astronomy, Monash University, Clayton 3800,
Victoria, Australia
7
LIGO Livingston Observatory, Livingston, LA 70754, United States of America
8
Max Planck Institute for Gravitational Physics (Albert Einstein Institute), D-30167
Hannover, Germany
9
Leibniz Universität Hannover, D-30167 Hannover, Germany
10
University of Cambridge, Cambridge CB2 1TN, United Kingdom
11
University of Birmingham, Birmingham B15 2TT, United Kingdom
12
LIGO, Massachusetts Institute of Technology, Cambridge, MA 02139,
United States of America
13
Instituto Nacional de Pesquisas Espaciais, 12227-010 São José dos Campos,
São Paulo, Brazil
14
Gran Sasso Science Institute (GSSI), I-67100 L’Aquila, Italy
7

## PDF page 9

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

15

INFN, Laboratori Nazionali del Gran Sasso, I-67100 Assergi, Italy
International Centre for Theoretical Sciences, Tata Institute of Fundamental
Research, Bengaluru 560089, India
17
NCSA, University of Illinois at Urbana-Champaign, Urbana, IL 61801,
United States of America
18
Università di Pisa, I-56127 Pisa, Italy
19
INFN, Sezione di Pisa, I-56127 Pisa, Italy
20
Departamento de Astronomía y Astrofísica, Universitat de València, E-46100
Burjassot, València, Spain
21
OzGrav, Australian National University, Canberra, Australian Capital Territory
0200, Australia
22
Laboratoire des Matériaux Avancés (LMA), CNRS/IN2P3, F-69622 Villeurbanne,
France
23
University of Wisconsin-Milwaukee, Milwaukee, WI 53201, United States of
America
24
SUPA, University of Strathclyde, Glasgow G1 1XQ, United Kingdom
25
LAL, Univ. Paris-Sud, CNRS/IN2P3, Université Paris-Saclay, F-91898 Orsay,
France
26
California State University Fullerton, Fullerton, CA 92831, United States of
America
27
APC, AstroParticule et Cosmologie, Université Paris Diderot, CNRS/IN2P3, CEA/
Irfu, Observatoire de Paris, Sorbonne Paris Cité, F-75205 Paris Cedex 13, France
28
European Gravitational Observatory (EGO), I-56021 Cascina, Pisa, Italy
29
Chennai Mathematical Institute, Chennai 603103, India
30
Università di Roma Tor Vergata, I-00133 Roma, Italy
31
INFN, Sezione di Roma Tor Vergata, I-00133 Roma, Italy
32
INFN, Sezione di Roma, I-00185 Roma, Italy
33
Laboratoire d’Annecy de Physique des Particules (LAPP), Univ. Grenoble Alpes,
Université Savoie Mont Blanc, CNRS/IN2P3, F-74941 Annecy, France
34
Embry-Riddle Aeronautical University, Prescott, AZ 86301,
United States of America
35
Montclair State University, Montclair, NJ 07043, United States of America
36
Max Planck Institute for Gravitational Physics (Albert Einstein Institute), D-14476
Potsdam-Golm, Germany
37
Nikhef, Science Park 105, 1098 XG Amsterdam, The Netherlands
38
Korea Institute of Science and Technology Information, Daejeon 34141,
Republic of Korea
39
West Virginia University, Morgantown, WV 26506, United States of America
40
Università di Perugia, I-06123 Perugia, Italy
41
INFN, Sezione di Perugia, I-06123 Perugia, Italy
42
Syracuse University, Syracuse, NY 13244, United States of America
43
University of Minnesota, Minneapolis, MN 55455, United States of America
44
SUPA, University of Glasgow, Glasgow G12 8QQ, United Kingdom
45
LIGO Hanford Observatory, Richland, WA 99352, United States of America
46
Caltech CaRT, Pasadena, CA 91125, United States of America
47
Wigner RCP, RMKI, H-1121 Budapest, Konkoly Thege Miklós út 29-33, Hungary
48
University of Florida, Gainesville, FL 32611, United States of America
49
Stanford University, Stanford, CA 94305, United States of America
50
Università di Camerino, Dipartimento di Fisica, I-62032 Camerino, Italy
51
Università di Padova, Dipartimento di Fisica e Astronomia, I-35131 Padova, Italy
52
INFN, Sezione di Padova, I-35131 Padova, Italy
53
Montana State University, Bozeman, MT 59717, United States of America
16

8

## PDF page 10

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

54

Nicolaus Copernicus Astronomical Center, Polish Academy of Sciences, 00-716,
Warsaw, Poland
55
OzGrav, University of Adelaide, Adelaide, South Australia 5005, Australia
56
Theoretisch-Physikalisches Institut, Friedrich-Schiller-Universität Jena, D-07743
Jena, Germany
57
INFN, Sezione di Milano Bicocca, Gruppo Collegato di Parma, I-43124 Parma,
Italy
58
Rochester Institute of Technology, Rochester, NY 14623, United States of America
59
Center for Interdisciplinary Exploration & Research in Astrophysics (CIERA),
Northwestern University, Evanston, IL 60208, United States of America
60
INFN, Sezione di Genova, I-16146 Genova, Italy
61
RRCAT, Indore, Madhya Pradesh 452013, India
62
Faculty of Physics, Lomonosov Moscow State University, Moscow 119991, Russia
63
OzGrav, University of Western Australia, Crawley, Western Australia 6009,
Australia
64
Department of Astrophysics/IMAPP, Radboud University Nijmegen, PO Box 9010,
6500 GL Nijmegen, The Netherlands
65
Artemis, Université Côte d’Azur, Observatoire Côte d’Azur, CNRS, CS 34229,
F-06304 Nice Cedex 4, France
66
Physik-Institut, University of Zurich, Winterthurerstrasse 190, 8057 Zurich,
Switzerland
67
Univ Rennes, CNRS, Institut FOTON—UMR6082, F-3500 Rennes, France
68
Cardiff University, Cardiff CF24 3AA, United Kingdom
69
Washington State University, Pullman, WA 99164, United States of America
70
University of Oregon, Eugene, OR 97403, United States of America
71
Laboratoire Kastler Brossel, Sorbonne Université, CNRS, ENS-Université PSL,
Collège de France, F-75005 Paris, France
72
Università degli Studi di Urbino ’Carlo Bo’, I-61029 Urbino, Italy
73
INFN, Sezione di Firenze, I-50019 Sesto Fiorentino, Firenze, Italy
74
Astronomical Observatory Warsaw University, 00-478 Warsaw, Poland
75
VU University Amsterdam, 1081 HV Amsterdam, The Netherlands
76
University of Maryland, College Park, MD 20742, United States of America
77
School of Physics, Georgia Institute of Technology, Atlanta, GA 30332,
United States of America
78
Université Claude Bernard Lyon 1, F-69622 Villeurbanne, France
79
Università di Napoli ’Federico II’, Complesso Universitario di Monte S.Angelo,
I-80126 Napoli, Italy
80
NASA Goddard Space Flight Center, Greenbelt, MD 20771,
United States of America
81
Dipartimento di Fisica, Università degli Studi di Genova, I-16146 Genova, Italy
82
RESCEU, University of Tokyo, Tokyo, 113-0033, Japan
83
Tsinghua University, Beijing 100084, People’s Republic of China
84
Texas Tech University, Lubbock, TX 79409, United States of America
85
The University of Mississippi, University, MS 38677, United States of America
86
Museo Storico della Fisica e Centro Studi e Ricerche ‘Enrico Fermi’, I-00184
Roma, Italyrico Fermi, I-00184 Roma, Italy
87
The Pennsylvania State University, University Park, PA 16802,
United States of America
88
National Tsing Hua University, Hsinchu City, 30013 Taiwan, Republic of China
89
Charles Sturt University, Wagga Wagga, New South Wales 2678, Australia
90
Canadian Institute for Theoretical Astrophysics, University of Toronto, Toronto,
Ontario M5S 3H8, Canada
91
University of Chicago, Chicago, IL 60637, United States of America
9

## PDF page 11

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

92

The Chinese University of Hong Kong, Shatin, NT, Hong Kong
Seoul National University, Seoul 08826, Republic of Korea
94
Pusan National University, Busan 46241, Republic of Korea
95
Carleton College, Northfield, MN 55057, United States of America
96
INAF, Osservatorio Astronomico di Padova, I-35122 Padova, Italy
97
INFN, Trento Institute for Fundamental Physics and Applications, I-38123 Povo,
Trento, Italy
98
OzGrav, University of Melbourne, Parkville, Victoria 3010, Australia
99
Columbia University, New York, NY 10027, United States of America
100
Universitat de les Illes Balears, IAC3—IEEC, E-07122 Palma de Mallorca, Spain
101
Université Libre de Bruxelles, Brussels 1050, Belgium
102
Sonoma State University, Rohnert Park, CA 94928, United States of America
103
Departamento de Matemáticas, Universitat de València, E-46100 Burjassot,
València, Spain
104
University of Rhode Island, Kingston, RI 02881, United States of America
105
The University of Texas Rio Grande Valley, Brownsville, TX 78520,
United States of America
106
Bellevue College, Bellevue, WA 98007, United States of America
107
MTA-ELTE Astrophysics Research Group, Institute of Physics, Eötvös University,
Budapest 1117, Hungary
108
Institute for Plasma Research, Bhat, Gandhinagar 382428, India
109
The University of Sheffield, Sheffield S10 2TN, United Kingdom
110
IGFAE, Campus Sur, Universidade de Santiago de Compostela, 15782,
Santiago de Compostela, Spain
111
Dipartimento di Scienze Matematiche, Fisiche e Informatiche,
Università di Parma, I-43124 Parma, Italy
112
California State University, Los Angeles, 5151 State University Dr, Los Angeles,
CA 90032, United States of America
113
Università di Trento, Dipartimento di Fisica, I-38123 Povo, Trento, Italy
114
Università di Roma ’La Sapienza’, I-00185 Roma, Italy
115
Colorado State University, Fort Collins, CO 80523, United States of America
116
Kenyon College, Gambier, OH 43022, United States of America
117
Christopher Newport University, Newport News, VA 23606, United States of
America
118
National Astronomical Observatory of Japan, 2-21-1 Osawa, Mitaka, Tokyo
181-8588, Japan
119
Observatori Astronòmic, Universitat de València, E-46980 Paterna, València, Spain
120
School of Mathematics, University of Edinburgh, Edinburgh EH9 3FD, United
Kingdom
121
Institute Of Advanced Research, Gandhinagar 382426, India
122
Indian Institute of Technology Bombay, Powai, Mumbai 400 076, India
123
University of Szeged, Dóm tér 9, Szeged 6720, Hungary
124
Tata Institute of Fundamental Research, Mumbai 400005, India
125
INAF, Osservatorio Astronomico di Capodimonte, I-80131, Napoli, Italy
126
University of Michigan, Ann Arbor, MI 48109, United States of America
127
American University, Washington, DC 20016, United States of America
128
GRAPPA, Anton Pannekoek Institute for Astronomy and Institute of High-Energy
Physics, University of Amsterdam, Science Park 904, 1098 XH Amsterdam, The
Netherlands
129
Delta Institute for Theoretical Physics, Science Park 904, 1090 GL Amsterdam,
The Netherlands
130
Directorate of Construction, Services & Estate Management, Mumbai 400094
India
93

10

## PDF page 12

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

131

University of Białystok, 15-424 Białystok, Poland
King’s College London, University of London, London WC2R 2LS,
United Kingdom
133
University of Southampton, Southampton SO17 1BJ, United Kingdom
134
University of Washington Bothell, Bothell, WA 98011, United States of America
135
Institute of Applied Physics, Nizhny Novgorod, 603950, Russia
136
Ewha Womans University, Seoul 03760, Republic of Korea
137
Inje University Gimhae, South Gyeongsang 50834, Republic of Korea
138
National Institute for Mathematical Sciences, Daejeon 34047, Republic of Korea
139
Ulsan National Institute of Science and Technology, Ulsan 44919, Republic of
Korea
140
Universität Hamburg, D-22761 Hamburg, Germany
141
Maastricht University, PO Box 616, 6200 MD Maastricht, The Netherlands
142
NCBJ, 05-400 Świerk-Otwock, Poland
143
Institute of Mathematics, Polish Academy of Sciences, 00656 Warsaw, Poland
144
Cornell University, Ithaca, NY 14850, United States of America
145
Hillsdale College, Hillsdale, MI 49242, United States of America
146
Hanyang University, Seoul 04763, Republic of Korea
147
Korea Astronomy and Space Science Institute, Daejeon 34055, Republic of Korea
148
NASA Marshall Space Flight Center, Huntsville, AL 35811,
United States of America
149
Dipartimento di Matematica e Fisica, Università degli Studi Roma Tre, I-00146
Roma, Italy
150
INFN, Sezione di Roma Tre, I-00146 Roma, Italy
151
ESPCI, CNRS, F-75005 Paris, France
152
OzGrav, Swinburne University of Technology, Hawthorn VIC 3122, Australia
153
University of Portsmouth, Portsmouth, PO1 3FX, United Kingdom
154
Southern University and A&M College, Baton Rouge, LA 70813,
United States of America
155
College of William and Mary, Williamsburg, VA 23187, United States of America
156
Centre Scientifique de Monaco, 8 quai Antoine Ier, MC-98000, Monaco
157
Indian Institute of Technology Madras, Chennai 600036, India
158
INFN Sezione di Torino, Via P. Giuria 1, I-10125 Torino, Italy
159
Institut des Hautes Etudes Scientifiques, F-91440 Bures-sur-Yvette, France
160
IISER-Kolkata, Mohanpur, West Bengal 741252, India
161
Whitman College, 345 Boyer Avenue, Walla Walla, WA 99362
United States of America
162
Université de Lyon, F-69361 Lyon, France
163
Hobart and William Smith Colleges, Geneva, NY 14456, United States of America
164
Janusz Gil Institute of Astronomy, University of Zielona Góra, 65-265 Zielona
Góra, Poland
165
University of Washington, Seattle, WA 98195, United States of America
166
SUPA, University of the West of Scotland, Paisley PA1 2BE, United Kingdom
167
Indian Institute of Technology, Gandhinagar Ahmedabad Gujarat 382424, India
168
Université de Montréal/Polytechnique, Montreal, Quebec H3T 1J4, Canada
169
Indian Institute of Technology Hyderabad, Sangareddy, Khandi, Telangana
502285, India
170
International Institute of Physics, Universidade Federal do Rio Grande do Norte,
Natal RN 59078-970, Brazil
171
Villanova University, 800 Lancaster Ave, Villanova, PA 19085,
United States of America
172
Andrews University, Berrien Springs, MI 49104, United States of America
173
Max Planck Institute for Gravitationalphysik (Albert Einstein Institute), D-14476
Potsdam-Golm, Germany
132

11

## PDF page 13

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

174

Università di Siena, I-53100 Siena, Italy
Trinity University, San Antonio, TX 78212, United States of America
176
Van Swinderen Institute for Particle Physics and Gravity, University of Groningen,
Nijenborgh 4, 9747 AG Groningen, The Netherlands
175

E-mail: lvc.publications@ligo.org
Received 9 September 2019, revised 4 December 2019
Accepted for publication 7 January 2020
Published 6 February 2020
Abstract

The LIGO Scientific Collaboration and the Virgo Collaboration have
cataloged eleven confidently detected gravitational-wave events during the
first two observing runs of the advanced detector era. All eleven events were
consistent with being from well-modeled mergers between compact stellarmass objects: black holes or neutron stars. The data around the time of each
of these events have been made publicly available through the gravitationalwave open science center. The entirety of the gravitational-wave strain data
from the first and second observing runs have also now been made publicly
available. There is considerable interest among the broad scientific community
in understanding the data and methods used in the analyses. In this paper, we
provide an overview of the detector noise properties and the data analysis
techniques used to detect gravitational-wave signals and infer the source
properties. We describe some of the checks that are performed to validate
the analyses and results from the observations of gravitational-wave events.
We also address concerns that have been raised about various properties of
LIGO–Virgo detector noise and the correctness of our analyses as applied to
the resulting data.
Keywords: gravitational waves, data analysis, gravitational wave detectors
(Some figures may appear in colour only in the online journal)
1. Introduction
Gravitational-wave observations have become an important new means to learn about the
Universe. The LIGO Scientific Collaboration and the Virgo Collaboration (LVC) have published a series of discoveries beginning with the first detected event, GW150914 [1], a binary
black hole merger. Within a span of two years, that event was followed by nine other binary
black hole detections (GW151012 [2, 3], GW151226 [4], GW170104 [5], GW170608 [6],
GW170729, GW170809, GW170814 [7], GW170818 and GW170823), and one binary neutron star merger, GW170817 [8]. Details about all of these confidently-detected gravitationalwave events have been published in a catalog, GWTC-1 [3].
The global gravitational-wave detector network currently consists of two Advanced LIGO
detectors in the U.S. [9] in Hanford, Washington and Livingston, Louisiana; the Advanced
177

Deceased, February 2018.
Deceased, November 2017.
179
Deceased, July 2018.
178

12

## PDF page 14

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Virgo detector in Cascina, Italy [10]; and the GEO 600 detector in Germany [11]. In the
coming years this network will grow through the addition of the Japanese detector, KAGRA
[12–14], and a third Advanced LIGO detector to be located in India [15]. The first observing
run (O1) of Advanced LIGO took place from September 12, 2015 until January 19, 2016. The
second observing run (O2) for the Advanced LIGO detectors began on November 30, 2016,
and lasted until August 25, 2017. The Advanced Virgo detector formally commenced observations in O2 on August 1, 2017, enabling the first three-detector observations of gravitational
waves [3]. A third LIGO–Virgo observing run, O3, began on April 1, 2019, with all three
detectors operating with their best sensitivity to date.
Consistency between multiple detectors helps greatly to suppress instrumental backgrounds and to allow coherent analysis of gravitational-wave signals. All of the event detections published to date have involved both of the Advanced LIGO detectors, while GW170814
and GW170818 were triple-detections sensed by Virgo as well. Data from Virgo were also
used in the parameter estimation analysis and sky localization determination for GW170729,
GW170809, and GW170817. The Virgo data were especially critical in helping to find the
source of GW170817 [16]. This binary neutron star merger represented a remarkable debut
for multi-messenger astronomy with gravitational waves, as it was closely followed by a short
gamma-ray burst, GRB 170817A [17, 18], and the relatively precise localization obtained
from the gravitational-wave data enabled the identification and thorough multi-wavelength
study of kilonova and afterglow emission from an optical counterpart, SSS17a / AT 2017gfo
[16, 19].
As summarized in [3], the LVC detections were made using two independent matchedfilter analyses to search for compact binary coalescences in O2 [20, 21], as well as an unmodeled search for short-duration transient signals or bursts [22]. Thus, detection methods that
were developed by the LVC and tested using simulated signals added to mock data, or to
previous sets of real data where any possible signals were overwhelmed by noise, have now
been demonstrated to be effective for astrophysical gravitational-wave signals. Testing and
validation of LVC analyses was achieved using both (simulated) signal injections performed
within the analysis, i.e. in software, and signal injections made in hardware by moving the
detectors’ test masses.
The growth of the number of observed gravitational-wave events has stimulated intense
interest in the astrophysical implications of the detected sources, as well as interest in the
gravitational-wave data. Currently, the LVC releases data through the Gravitational-Wave
Open Science Center (GWOSC) [23, 24]. LIGO data releases are described in the LIGO Data
Management Plan [25], an agreement between the LIGO Laboratory and the US National
Science Foundation. The LVC policy for releasing gravitational-wave triggers and event candidates is presented in [26, 27]. For detections of compact binary mergers, about one hour
(4096 s) of calibrated strain data around the event time are released at the time of publication.
These data are available for all published detections in O1 and O2 [28].
Currently the bulk data from the initial LIGO Science Runs since 2005 are available
on GWOSC [24], as are the Advanced LIGO data from the O1 observing run [29] and the
Advanced LIGO and Advanced Virgo data from the O2 observing run [30]. Timing for release
of data in future observing runs is described in the Data Management Plan [25]; for instance,
the bulk data from the first 6 months of the O3 run will be released in April 2021. GWOSC
is continually updating and releasing data products that address the needs and interests of the
broader scientific community. Many of the analysis software packages used by the collaboration are publicly available as open source code; a list of these is available on the GWOSC
web site [24]. Also, a number of intermediate data products are released through the LIGO
Document Control Center, typically linked with LVC papers; e.g. see [31].
13

## PDF page 15

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 1. A simplified schematic summarizing the main steps in LIGO–Virgo data
processing, from the output of the data to the results reported in a catalog of transient
events.

With the public release of the LIGO and Virgo data, groups outside these collaborations
are analyzing the released data. Most of these analyses are producing results consistent with
the LVC’s [32–39], and some additional significant event candidates have been reported [40,
41]. The noise properties of the LIGO data and the correctness of the LVC data analysis
for GW150914 have also been questioned [42, 43], although successive gravitational wave
detections have strengthened confidence in our detection and parameter estimation methods
[3]. Motivated by the widespread interest in analyzing LIGO and Virgo data, in this paper we
provide an overview of the properties of the LIGO–Virgo data and its noise components. We
also describe the essential features of data analysis procedures that have been used by LIGO
and Virgo teams to detect and measure the properties of the cataloged gravitational-wave
sources [3], as summarized in figure 1. The analysis of LIGO and Virgo data in searching for
gravitational-wave signals is complex, as is the correct treatment of the statistical properties
of noise. The LVC encourages the broader scientific community to access and analyze its
data, and will always be open to discussions about the methods it uses to arrive at its conclusions. The codes used to analyze LIGO–Virgo data are public. The special purpose codes
used to generate many of the figures in this paper are also available [44]. In addition, the LVC
has made available a Jupyter notebook to illustrate methods used to produce key figures and
results in a simplified implementation [45]. Finally, many of the software packages used by
the LVC to process the LIGO–Virgo data, search for events and characterize observed signals
can be found at the GWOSC site [46].
The paper is organized as follows. In section 2 we describe the properties of the LIGO–
Virgo data, while in section 3 we discuss the noise that affects those data. Section 4 describes
14

## PDF page 16

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

the basic data processing steps used to properly Fourier transform the data and estimate the
power spectrum. Section 5 describes wavelet based time-frequency methods that can be used
to assess possible deviations from stationary detector noise. Section 6 addresses detector and
calibration issues for LIGO and Virgo. Section 7 describes the noise model used to define the
likelihood function used in parameter estimation studies. Section 8 gives a description of the
means by which the LVC searches for gravitational-wave signals, while section 9 presents the
means by which the LVC infers the detected waveforms and estimates the physical parameters
for the system that emitted the gravitational waves. To illustrate these concepts, section 10
provides a simplified description of how the publicly released data surrounding GW150914
can be used to find a best fit waveform model and to study the correlation properties of the
residuals. We also address claims made in [42, 43] concerning correlations in detector noise,
residuals, and the estimation of GW150914’s source properties. In addressing these claims,
the LVC notes that it is beneficial for gravitational-wave science that groups external to our
collaboration can introduce new ideas and techniques. Finally, in section 11 we provide a
summary assessment of LIGO and Virgo data properties as well as LVC data analysis findings
and validation.
2. Properties of LIGO–Virgo data
The Advanced LIGO [9] and Advanced Virgo [10] second-generation gravitational-wave
detectors are large-scale enhanced Michelson interferometers. The detectors are sensitive to
space time strain induced by passing gravitational waves, as well as equivalent terrestrial force
and displacement noises, each causing the lengths of the arms to vary over time. Differences in
relative arm length generate power variations in the enhanced Michelson’s output, captured by
photodiodes. The signal from these photodiodes serve as both the gravitational-wave readout
and an error signal for controlling the relative arm length below roughly 100 Hz.
The Advanced LIGO gravitational-wave detectors are identical in design, with 4 km long
arms. Advanced Virgo has a similar design, with 3 km long arms. Fabry–Perot cavities are
used in the arms of the detectors to increase the interaction time with a gravitational wave, and
power recycling is used to increase the effective laser power. Signal recycling has been added
in the Advanced LIGO detectors to shape their frequency response [9]. Advanced Virgo has
not yet implemented signal recycling, but will in the future [10].
A calibration procedure is applied to the interferometer photodiode output of each detector
(see section 6.1) to produce gravitational-wave strain data as a time series, sampled at 16384
Hz for LIGO data and 20 kHz for Virgo data. For the Advanced LIGO detectors, the calibration is valid above 10 Hz and below 5 kHz, as described in section 6.1. For Advanced Virgo
in O2 the calibration validity range was from 10 Hz to 8 kHz [47]. The detectors also record
hundreds of thousands of auxiliary channels, time series recorded in addition to the strain signal, that monitor the behavior of the detectors and their environment. The GWOSC provides
distilled additional channels of data in which flags pertaining to different levels of problems
with the data quality are implemented180. We employ continuous monitoring of the detector
performance to characterize noise sources that could negatively impact the sensitivity of the
searches or the source property estimation [48, 49]. Invalid data due to detector malfunction,
calibration error, or data acquisition problems are flagged so that they can be removed from
analyses, as described in section 6 and [50].

180

www.gw-openscience.org/segments
15

## PDF page 17

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

3. Basic properties of detector noise
The data recorded by the Advanced LIGO and Advanced Virgo instruments are impacted by
many sources of noise, including quantum sensing noise, seismic noise, suspension thermal
noise, mirror coating thermal noise, and gravity gradient noise [9]. In addition, there are transient noise events, for example coming from anthropogenic sources, weather, equipment malfunctions [48], as well as occasional transient noise of unknown origin [51]. There is also
persistent elevated noise confined to certain frequencies, manifesting as very narrow peaks
in a plot of noise versus frequency, which we refer to as spectral lines; these are typically
caused by electrical and mechanical devices or resonances [49]. The combination of all the
noise sources in a detector produces a time series n(t) that can be represented by a vector n ,
with components given by the discrete time samples ni = n(ti ). The noise is described as a
stochastic process with statistical properties given by the joint probability distribution p(n).
This model can be used to define summary statistics such as the mean µ = E[n] (where E is
defined as the expectation value) and covariance Cij = E[(ni − µ)(nj − µ)] where the expectation values are taken with respect to p(n). The mean can be estimated from the data as
1 ∑
ni ,
N
N

µ̂ =

(1)

i=1

where N = dim(n) is the number of data samples. The full covariance matrix cannot be estimated from the data without making additional assumptions as we have only M = 1 measurements for each data point, rendering the sample covariance matrix formally undefined:
Ĉij =

1
(ni − µ̂)(nj − µ̂) .
M−1

(2)

Estimates of the covariance matrix can be made if noise is assumed to follow a particular
distribution, or if the noise properties are unchanging in time. Note that in practice, analyses
generally do not use all N samples at once, but rather use segments of contiguous data of
various lengths from a few seconds up to hours depending on the intended application. Noise
is referred to as Gaussian if the joint probability distribution follows a multi-variate normal
distribution:


∑
1
1
p(n) =
(ni − µ)(nj − µ)Cij−1  ,
exp −
(3)
2 ij
det(2πC)1/2
where Cij−1 is the inverse of the covariance matrix at i, j. The noise is referred to as stationary
if Cij depends only on the lag |i − j|. Stationary noise is characterized by the correlation function C(τ ), where τ = |ti − tj | is the time lag. Transforming to the Fourier domain, where the
labels i, j now refer to frequencies fi , fj , stationary noise has a diagonal covariance matrix
Cij = δij Sn ( fi ), which defines the power spectral density Sn(f ). The power spectral density is
given by the Fourier transform of the correlation function C(τ ). Amplitude spectral density is
the square root of power spectral density and has units of Hz−1/2. The noise is referred to as
white if Cij = δij σ 2 in both the frequency domain and the time domain. White noise is, however, a poor approximation to LIGO–Virgo detector noise
Understanding the noise is crucial to detecting gravitational-wave signals and inferring
the properties of the astrophysical sources that generate them. Improper modeling of the
noise can result in the significance of an event being incorrectly estimated, and to systematic biases in the parameter estimation. To guard against these unwanted outcomes, detector
16

## PDF page 18

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

characterization and noise modeling are significant activities within the LVC [48, 50]. While
many textbook treatments of gravitational-wave data analysis [52–54] describe the idealized
case of independent detectors with stationary, Gaussian noise, actual LVC analyses are careful
to account for deviations from this ideal.
The Advanced LIGO and Advanced Virgo detector data have a rich structure in both time
and frequency. For a given gravitational-wave source, the noise (as described by its spectral
density) governs the measured signal-to-noise ratio (SNR). Figure 2 shows the spectral frequency content of the LIGO-Livingston detector averaged over a three minute period shortly
before the first detection of gravitational waves from a binary neutron star merger, GW170817.
During the O1 and O2 runs, the Advanced LIGO detectors had an averaged measured noise
amplitude of about 10−23 Hz−1/2 at 100 Hz. (The target sensitivity at 100 Hz for Advanced
LIGO is 4 × 10−24 Hz−1/2 [9], while for Advanced Virgo it is 5 × 10−24 Hz−1/2 [10].) The
steep shape at low frequencies is dominated by noise related to ground motion. Above roughly
100 Hz, the Advanced LIGO detectors are currently quantum noise limited, and their noise
curves are dominated by shot noise [9, 55]. High amplitude noise features are also present in
the data at certain frequencies, including lines due to the AC power grid (harmonics of 60 Hz
in the U.S. and 50 Hz in Europe), mechanical resonances of the mirror suspensions, injected
calibration lines, and noise entering through the detector control systems. For a detailed
account of noise sources that appear at specific frequencies in the Advanced LIGO detectors,
see [49]. For a list of the Advanced Virgo noise lines for observing run O2, see [56].
4. Fourier domain analysis
The noise in the LIGO–Virgo detectors is, with isolated exceptions, approximately stationary, and therefore can be most easily characterized in the frequency domain. Stationary,
Gaussian noise is uncorrelated between frequency bins, and the noise ñ( f ) in each bin follows
1/2
a Gaussian distribution with random phase and amplitude Sn ( f ). The first step in many
LVC analyses is to Fourier transform the time-domain data using a fast Fourier transform
(FFT) [57–59]. Since the FFT implicitly assumes that the stretch of data being transformed is
periodic in time, window functions [60, 61] have to be applied to the data to suppress spectral
leakage [61] using e.g. a Tukey (cosine-tapered) window function. Failing to window the
data will lead to spectral leakage and spurious correlations in the phase between bins. For the
analysis of transient data the use of Tukey windows is advantageous as signals will suffer less
modification than, for example, Hanning or Flattop windows [61].
As an illustration, figure 3 shows a sequence of processing steps applied to a stretch of calibrated strain data from the LIGO-Hanford detector around the time of GW150914. The raw
data are dominated by low-frequency noise. A Tukey window with 0.5 s transition regions was
applied to the raw data. Next, the data were whitened by dividing the Fourier coefficients by
an estimate of the amplitude spectral density of the noise, which ensures that the data in each
frequency bin has equal significance by down-weighting frequencies where the noise is loud.
The data were then inverse Fourier transformed to return to the time domain:
FFT

d̃( f )

Whiten

d(t) −→ d̃( f ) −→ d̃w ( f ) =

1/2
Sn ( f )

iFFT

−→ dw (t) .

(4)

The whitened samples were scaled to have unit variance in the time domain. As a final step,
the data were bandpass filtered using a zero-phase, eighth order Butterworth filter with pass
band [35 Hz, 350 Hz]. The bandpass enhances the visibility of features of interest in this band
17

## PDF page 19

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 2. Amplitude spectral density of the LIGO-Livingston detector data, using 10 s

fast Fourier transforms and averaged over a three minute period starting at August 17,
2017 12:36:00 UTC, five minutes before the merger time of GW170817 [8]. The top
plot is a linear frequency scale, highlighting periodic features from 0 Hz to 2000 Hz.
The bottom plot is a log scale, illustrating the features in the detector data from 8 Hz to
the Nyquist frequency 8192 Hz.

by removing noise outside of the band—seismic and related noise at low frequencies, and
quantum sensing noise at high frequencies. Note that such narrow bandpassing is only used
for visualization purposes and is not employed in the LVC analyses. The gravitational-wave
signal GW150914 is visible in the whitened and bandpassed data shown in the lower panel
of figure 3.
While the steps above can make loud transient signals like GW150914 more easily visible
in the strain time series, LVC’s statistical analysis pipelines typically use a different sequence
of processing steps. LVC pipelines for detection and parameter estimation proceed by first
high-pass filtering the data, to remove high-amplitude noise below the range of frequencies
that will be analyzed by the pipelines which typically starts at ∼20 Hz. The data may also be
down-sampled, after low-pass filtering to avoid aliasing, to reduce computational costs; thus
its frequency content will be affected by the anti-aliasing filter at high frequency, with a formal
cutoff at the Nyquist frequency of the down-sampled data [20, 21]. The LVC parameter estimation pipelines do not apply any bandpass filter to the data, but limit the likelihood integral
calculation to begin at some lower frequency cut-off (typically also 20 Hz).
GW150914 was originally identified with high significance by a generic search for coherent excess power across the detector network [1, 62], as well as by matched-filtering analyses
[2], as described in section 8, but this loud signal is also clearly visible in the data even with
the minimal processing described here.
18

## PDF page 20

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 3. A sequence of processing steps applied to the calibrated strain from the LIGOHanford detector showing 4 s of data centered on GPS time 1126259462 (September
14, 2015 09:50:45 UTC). First a Tukey window with 0.5 s roll-off is applied, then the
data are whitened using an estimate of the noise spectral density. Finally the data are
bandpassed filtered to enhance features in the passband [35 Hz, 350 Hz], revealing the
presence of gravitational-wave signal GW150914.

4.1. Methods for measuring the noise spectrum

The power spectral density of the noise Sn(f ) is not known a priori and must be estimated from
the data. One can perform a complex FFT of the entire data stream around some time to be
searched for signals, but that yields only two samples (real and imaginary parts) per frequency
bin, hence the variance in the estimate of Sn(f ) in any single frequency bin is large. To overcome this, either some form of averaging is used [63], or a fit is made to a physical model for
the spectrum [64]. For example, Welch averaging [65] can be used to reduce the variance in
the estimated power spectrum, but at the cost of either reducing the frequency resolution or
requiring longer stretches of data. The spectral estimate used to whiten the data in figure 3 was
found by applying a Welch average to 1024 s of data centered on GPS time 1126259462 (the
nearest integer GPS time to the peak of the GW150914 signal). The data were broken up into
overlapping 4 s long chunks, each spaced by 2 s. The data in each chunk was Tukey filtered
and Fourier transformed. The power spectrum from all the chunks was then averaged.
19

## PDF page 21

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 4. Power spectral density for the data shown in figure 3. The spectrum for the
non-windowed data are swamped by spectral leakage, and follow a 1/f 2 scaling. The
Welch average was computed using a longer stretch of data.

Figure 4 compares the power spectrum of the Hanford data shown in figure 3, before and
after applying the Tukey window, to the power spectrum estimated using Welch averaging.
The non-windowed spectrum is swamped by spectral leakage, and follows a 1/f 2 scaling. This
scaling results from the abrupt step function at the beginning and end of the data to be Fourier
transformed. This non-windowed data chunk arises from multiplying a longer stretch of data
by a boxcar (or top hat) window. Thus, when it is Fourier transformed, the result is the convolution of the desired spectrum of the original data with the Fourier transform of the 4s-long
boxcar window, i.e. a cardinal sine (sinc) function whose amplitude decreases as 1/f 2. Since
the noise spectrum rises much more rapidly than 1/f 2 towards low frequencies, the entire visible frequency range is then dominated by the leakage from this low-frequency component.
When the noise spectrum varies significantly over time other spectral estimation methods
have to be used [20, 66]. One approach used in LVC parameter estimation studies is to fit a
parametrized spectral model to the data that has a smooth spline component and a collection
of Lorentzian lines [64]. In section 5 we also discuss in detail the issue of stationarity and nonstationarity of the data, and the effects this has on the data analysis.
In addition to causing spectral leakage, improper windowing of the data can result in spurious phase correlations in the Fourier transform. Figure 5 shows a scatter plot of the Fourier
phase as a function of frequency for the same stretch of data shown in figure 4, both with and
without the application of a window function. The un-windowed data shows a strong phase
correlation, while the windowed data does not.
The degree to which a time series is consistent with being stationary and Gaussian noise can
be diagnosed by looking at the distribution of its Fourier transformed frequency samples. If
the noise is stationary and Gaussian the real and imaginary parts of the whitened noise in each
frequency bin will be a collection of independent and identically distributed (i.i.d.) random
variables with zero mean and unit variance: x ∼ N (0, 1). Departures from stationarity result
20

## PDF page 22

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 5. The Fourier phases of the stretch of LIGO-Hanford data shown in figure 3. If
no window is applied before performing the FTT, as was the case in the analysis in [42],
spectral leakage causes the phase to be correlated. When the Tukey window is applied
the phases appear randomly distributed, as expected for Gaussian noise. The phases
show some clustering around the 60 Hz power line, consistent with the deterministic
origin of this noise component.

in correlations between samples in different Fourier bins, while departures from Gaussianity
can be identified by comparing the distribution of samples to a unit normal distribution. Loud
instrumental noise transients and loud gravitational-wave bursts do contribute to non-stationary and non-Gaussian features, but away from these transient disturbances the LIGO–Virgo
data can be approximated as stationary and Gaussian. Figure 6 shows the whitened Fourier
amplitudes for a quiet stretch of data from the LIGO-Livingston observatory.
5. Time-frequency analysis and stationarity
The LIGO–Virgo data exhibit two main types of non-stationary behavior. The first is slow
and continuous adiabatic drifts in the power spectrum occurring over minutes or hours, and
the second is short-duration noise transients, which we refer to as glitches, that are typically
localized in time and frequency. Additional non-stationarity has been observed in the vicinity
of spectral lines, such as those due to electromagnetic couplings to the 50/60 Hz AC power
supply. The adiabatic drifts in the power spectrum can be defined in terms of locally stationary
processes [67, 68]. A locally stationary process has a covariance function which is the product
of a covariance function for a stationary process and a time-variable function.
The stationarity of the data is evaluated as part of candidate event validation [3, 48].
Here we describe some simplified non-stationarity tests that can be applied to the data. Nonstationarity can in principle be identified by looking for correlations in the Fourier amplitudes,
but it is easier to identify and classify non-stationary behavior using time-frequency methods.
The simplest approach is to divide the data into small chunks of time centered on time ti, and
compute a smoothed estimate for the power spectrum for each chunk Sn ( f , ti ). Figure 7 shows
21

## PDF page 23

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 6. The panel on the left shows a 2-d density plot of the whitened real and

imaginary Fourier amplitude deviations using 256 s of LIGO-Livingston data centered
on GPS time 1186741733 covering the band from 32 Hz to 512 Hz. The panel on the
right shows a 1-d histogram of the Fourier amplitudes. The solid line is for a reference
N (0, 1) distribution, while the dashed lines indicate the expected 3-sigma variance
from having a finite number of samples.

Figure 7. Power spectral density (solid lines) with 90% credible intervals (shaded

bands) for the LIGO-Hanford detector computed using 8 s stretches of data spaced
by 64 s intervals starting at GPS time 1165067724. During this time period there was
significant broad-band non-stationarity between 32 and 256 Hz.

Bayesian power spectral density estimates [64] computed using 8 s stretches of data from the
LIGO-Hanford instrument that are spaced at 64 s intervals. The instrument noise level was
highly variable during this time period, showing large changes in the power spectral density in
the band between 32 Hz and 256 Hz (note that this particular period of time for this example
was chosen due to observed large variations in the detector’s sensitivity).
Wavelets provide a more flexible analysis framework than short-time Fourier transforms.
Continuous wavelet transforms are commonly used in LIGO–Virgo data studies to produce
22

## PDF page 24

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 8. Fluctuations in the whitened data for the same stretch of highly nonstationary LIGO-Hanford data used to produce figure 7. The data were first whitened
using an amplitude spectral density estimated from 256 s of data centered at GPS time
1165067917, then a discrete wavelet wavepacket transform was used to produce the
scalogram shown in the lower panel. The upper panel shows the average power as a
function of time computed from the scalogram.

spectrograms that provide a visual indication of non-stationary behavior. Quantitative assessments of non-stationarity may also be made by using discrete, orthogonal wavelet transforms.
These can be visualized using a scalogram, showing the amplitudes of the wavelet basis functions at each discrete time and frequency pixel. Figure 8 shows a scalogram of the same stretch
of LIGO-Hanford data which were used to produce figure 7. The data were first whitened
using an amplitude spectral density estimate taken from 256 s of data centered at GPS time
1165067917. The whitened data were then transformed using discrete wavepackets181, built
from Meyer wavelets [70], that were chosen to give uniform time and frequency coverage with
tiles of size ∆t = 0.5 s and ∆f = 1 Hz. The average power at each time was then computed
by summing the squares of the wavelet amplitudes (and dividing by a normalization constant)
between 16 and 256 Hz. The noise level is elevated for almost a minute around the center of
the data segment.
When this analysis is applied to stationary, Gaussian noise, the power in each time interval
follows a chi-squared distribution with Nf degrees of freedom, where Nf is the number of frequency pixels that are summed over. The distribution of the average power can be compared
to this reference distribution using e.g. an Anderson–Darling test [71], to yield a quantitative
measure of the non-stationarity. Note that while stationary noise is stationary no matter what
time span is considered, non-stationary noise will produce different measures of departure
depending on the averaging scale (here the width of the wavelet pixels in time) and time span
181

Note that the standard discrete wavelet transformation applies successive high and low pass filters in a particular
order. The wavelet wave packet transform generalizes this to consider all possible combinations of filter application
orders. A particular path through this transformation sequence defines some wavelet wave packet transformation.
One is free to choose the decomposition path. Various criteria can be used to select an optimal or near optimal decomposition for a particular data set. In the study presented in this paper we use a path that gives a regular spacing
in frequency bands because this choice provides a simple generalization of a discrete Fourier transform to the more
flexible time-frequency case. For more information on this method, see [69].
23

## PDF page 25

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 9. A quiet stretch of whitened strain data from the LIGO-Livingston laboratory

centered on GPS time 1186741733. The upper panel shows the transformed average
power statistic s(t) for a variety of wavelet resolutions (plotted in different colors)
with pixels ranging from 0.25 s to 2 s in width. The power fluctuations s(t) should
follow a zero mean, unit variance Gaussian distribution when the noise is stationary and
Gaussian. The lower panel shows a wavelet scalogram at 0.5 s resolution.

Figure 10. A stretch of whitened strain data from the LIGO-Livingston laboratory
centered on GPS time 1166358283. The upper panel shows the transformed average
power statistic s(t) for a variety of wavelet resolutions with pixels ranging from 0.25
s to 2 s in width. The power fluctuations s(t) should follow a zero mean, unit variance
Gaussian distribution when the noise is stationary and Gaussian. The lower panel shows
a wavelet scalogram at 0.5 s resolution. A series of glitches causes significant nonstationarity.

24

## PDF page 26

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

of the data. For visualization purposes it is convenient to transform the average power p(t) to a
new variable s(t) via the Wilson–Hilferty transformation [72], such that s(t) follows a N (0, 1)
Gaussian distribution when the noise is stationary and Gaussian.
Applying the Anderson–Darling test to the total power yields p -values for the hypothesis
that the data are stationary. When applied to the quiet stretch of data shown in figure 9 the test
yields a p-value of p = 0.74, indicating that the hypothesis that the data are stationary cannot be rejected over this time period at this wavelet scale. Applying the same test to the data
shown in figure 10 yields a p -value of p = 2.3 × 10−6 , and we can reject the hypothesis that
the data are stationary with high confidence. Any analysis that attempted to detect or estimate
the parameters of a possible gravitational-wave signal occurring in this stretch of data would
then have to take steps to mitigate, suppress or otherwise account for the departure from stationary noise.
6. Detector calibration and data quality
In this section we provide the central concepts related to the calibration of the data as well as
an overview of the data quality checks we perform. These procedures ensure that the strain
data used for analyses (namely, the analyses used by the LVC in publication results) and made
public on the GWOSC is calibrated properly with known error bars, and that time periods of
poor data quality can be avoided, as explained below.
6.1. Detector calibration

The Advanced LIGO [9, 55, 73, 74] and Advanced Virgo [10, 47, 75] detectors use feedback
loops to keep the optical cavities on resonance. The strain calibration must thus include models and measurements of all readout electronics, as well as of electronics and transfer functions of actuation hardware that act on the mirrors through multiple points in the suspension
systems [76]. As shown in figure 11, there are three main components of the differential arm
control loop for Advanced LIGO: the actuation function A( f ), the sensing function C( f ), and
the digital filters applied, D( f ). All three are measured and modeled as functions of frequency.
The digital filters are known to great precision so the calibration error and uncertainty come
from the differences between the model and measurement (including measurement error) of
the actuation and sensing functions, A and C. To independently measure the actuation and
sensing functions, a pair of beams from auxiliary lasers are reflected off of each test mass
mirror, with their intensities modulated at a known frequency and amplitude to actuate with
radiation pressure. These auxiliary laser assemblies are referred to as photon calibrators [77].
Once A and C are known, the true differential arm length is extracted and translated to a strain
by dividing by the common length of the arm L (4 km for LIGO, 3 km for Virgo), per the following equation:
h(t) =

]
1 [ −1
C ∗ derr (t) + A ∗ dctrl (t) ,
L

(5)

where C and A are time-domain filters derived from frequency-domain measurements of the
actuation function A( f ) and the sensing function C( f ).
Note that the gravitational-wave strain can also appear in the common-mode arm length
changes, and in changes to the lengths of all degrees of freedom in the detector. However, only
the sensing of the differential change in the interferometer’s arm lengths is engineered to have
low enough instrumental noise to be sensitive to the strain induced by gravitational waves. The
25

## PDF page 27

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 11. Differential arm length control loop and calibration diagram of the LIGO
detectors from the GW150914 companion paper on calibration [55]. The left (grey) box
shows the realtime detector controls while the right (purple) box shows the calibration
procedure. ∆Lfree is the unsuppressed change in differential arm length, and hence
the desired quantity. The photodiodes (part of the sensing C) measure the residual
differential arm length ∆Lres, which is suppressed by the feedback loop. The ‘error
signal’ derr, equal to ∆Lres multiplied by the sensing function C, is passed through digital
filters, D, and applied to the differential arm length actuators through the actuation
function, A. In order to reconstruct an estimate of ∆Lfree in units of strain we model A
(PC)
and C, denoted in the purple box. xT denotes where in the loop we apply a force to
the test mass mirrors, via radiation pressure (photon calibrator), in order to measure A
and C, as functions of frequency. The output of the calibration pipeline is then a strain
signal, h(t), that is a faithful representation of ∆Lfree /L.

other optical lengths are controlled in order to maintain an optimal and linear response to the
gravitational-wave strain in the differential degree of freedom.
Calibration measurements are made periodically in each observing run. In addition, to
monitor time dependent parameters such as optical gain, cavity pole frequency and actuation
strength drifts, several calibration lines are continously injected, at specific frequencies, by
applying sinusoidal forces on the test mass mirrors using the photon calibrators; these lines
will be present in the raw strain data. The calibration line frequencies are different amongst
the detectors.
For the second observing run O2 and onwards, the calibration lines are removed from the
calibrated h(t) strain data channel (within the calibration accuracy) [47, 78]; the calibration
lines were not removed from the O1 data [74]. Even for O1, the presence of the calibration
lines does not affect the search for compact binary coalescence gravitational-wave signals as
the amplitude of data at the frequencies of the lines is suppressed via the whitening [79, 80] of
the data when the calculation of the detection statistic is made for the data from each detector
(see section 8). Similarly, for parameter estimation the presence of the noise spectral density
in the likelihood (see section 9) minimizes the influence of spectral lines including calibration
lines. Because the spectral lines are narrow, this frequency-domain weighting has a negligible
effect on signal searches and parameter estimation and does not lead to any spurious effects
such as generation of false candidate events or parameter biases.
26

## PDF page 28

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

For the Advanced Virgo calibration in O2 it was necessary to account for the transfer function of the optical response of the interferometer. This requires a calibration of the longitudinal actuators for the mirrors, still based on the laser wavelength as length reference using
the so-called free swinging Michelson configuration described in [81]. In addition, the interferometer’s output power as determined by the readout electronics also requires calibration.
Calibration measurements are made weekly in each observing run and have shown stable
actuation strengths. To monitor the time dependent optical gain and cavity pole frequency,
several calibration lines are continously injected, as in LIGO detectors, at specific frequencies,
by applying sinusoidal forces on the test mass mirrors using the electro-magnetic actuators.
By construction, the calibration lines are removed from the calibrated h(t) strain data channel (within the calibration accuracy). For Advanced Virgo in O2 the gravitational wave strain
reconstruction removed the contributions from control signals to the test mass mirror motion.
A photon calibrator, namely an auxiliary laser that is used to reflect photons off a mirror and
induce momentum transfer, was used to verify the calibration and confirm the sign of the
strain channel h(t). See [47] for more explicit details of the Advanced Virgo calibration system
for O2.
Calibrated strain data for the LIGO and Virgo detectors are created online for use in lowlatency searches. After the completion of the observing runs, final time-dependent calibrations
were generated for each detector. The results presented in GWTC-1 [3] use the full frequencydependent calibration uncertainties described in [47, 82, 83]. It is important to note that the
detector strain channel h(t) is only calibrated between 10 Hz and 5 kHz for Advanced LIGO
and 10 Hz and 8 kHz for Advanced Virgo [47]; the channel is not a faithful representation of
strain at lower or higher frequencies.
6.2. Data quality and terrestrial noise

As described in sections 3 and 5, calibrated LIGO and Virgo data can be both non-stationary
and non-Gaussian at certain times and frequencies. Glitches may mimic true transient astrophysical signals in individual detectors [48], while spectral lines such as those seen in figure 2
can blind searches for long-duration signals at those specific frequencies [49]. In this section we outline how we identify and characterize these noise features so that we can either
exclude the bad data or assess the impact of remaining artifacts on searches for gravitationalwave signals.
Figure 12 shows an example of a glitch. Glitches with power comparable to detectable signals have historically occurred on the order of once per minute, with larger glitches occurring
less frequently. Even in their nominal state, the detectors’ data contain glitches introduced by
behavior of the instruments or complex interactions between the instruments and their environment. Many of these glitches (but not all) can be associated with transient signals in auxiliary channels from various sensors which serve as ‘witnesses’ to environmental disturbances
coupling into the interferometer. These associations allow us to identify and catalog certain
classes of glitches. See [48] for a detailed presentation on the characterization of transient noise
in Advanced LIGO, especially pertaining to the observation of the gravitational-wave signal
GW150914. Descriptions of various noise sources for Advanced Virgo in O2 can be found in
[84–87].
In searches for transient gravitational-wave signals, identified glitches and periods of poor
data quality are flagged [50, 88, 89]. Periods of data are vetoed at various levels or categories
depending on the severity of the problems; the GWOSC open data releases make this information available [24]. Sections of strongly non-stationary data that would corrupt the noise
27

## PDF page 29

B P Abbott et al

1024

25

512

20

256

15

128
64

10

32

5

Normalized energy

Frequency [Hz]

Class. Quantum Grav. 37 (2020) 055002

16
0
-100-80 -60 -40 -20 0 20 40 60 80 100
Time [milliseconds]
Figure 12. Spectrogram of an example of transient noise in the advanced detectors;

a blip glitch in LIGO-Livingston. This is a zoomed image of the blip glitch shown in
figure 10 of [50].

power spectral density estimates are removed entirely from the searches. Times when noise
sources with known physical coupling to the gravitational-wave strain channel of the detector
are active, and thus likely to cause glitches, are identified, and candidates at or around these
times may be removed (vetoed) from search results. For a more detailed explanation of the
strategy for mitigating noise sources, see section 4 of [48]. For searches for long-duration
signals, frequency bands known to be dominated by instrument noise are omitted from the
analysis [49]. The strategy of vetoing times of probable glitches is expected to increase confidence in detection candidates that survive the application of vetoes [50, 90, 91], and may
thus increase the number of astrophysical signals that can be confidently detected. Detection
methods are discussed in detail in section 8.
Although the great majority of transient noise sources are of local origin and thus uncorrelated between detectors, some noise sources exist that are potentially correlated between
detectors, such as electromagnetic pulses from lightning coupling inductively into the detectors [92]. A key feature of the LIGO and Virgo experimental design is an array of physical
environment monitors designed to detect environmental disturbances, and to have greater sensitivity to those disturbances than the detector’s gravitational-wave strain channel does. The
LIGO environmental sensor array includes seismometers, microphones, accelerometers, radio
receivers and magnetometers to monitor ambient noise [93]182. Virgo has a similar array of
sensors [10]183. The environmental sensors’ sensitivities are verified via a suite of noise injections performed at the beginning and end of each observing run; acoustic, magnetic, radio
frequency, and vibrational tests are done to quantify the coupling from ambient noise to the
gravitational-wave strain data h(t) [48]. These injections are conducted at multiple locations
around the detector such that sensor coupling functions to h(t) via multiple potential coupling
paths are verified and well understood.
As shown in figure 2 of [48], the external transient electromagnetic coupling of the ambient
noise to the gravitational-wave data channel h(t) is on the order of a factor of 100 below the
182
183

See also http://pem.ligo.org
See also https://tds.virgo-gw.eu/?content=3&r=15647
28

## PDF page 30

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

current strain level, such that any electromagnetic source would have to register in one of the
magnetometers surrounding the detector an SNR of 100 before registering in the gravitationalwave signal channel. This is easily confirmed with the study of lightning strikes during nearby
storms [48]. The description of the coherence between the detectors’ output strain signal h(t)
and magnetometers about the detector for the AC power frequencies (50/60 Hz) is nontrivial
and described in [94]. In Virgo, a detailed study of the electromagnetic coupling to the gravitational-wave data channel was recently carried out [84, 85].
In addition, a potential correlated noise source in searches for a stochastic gravitationalwave background is Schumann resonances, or low-frequency magnetic field resonances
between the Earth’s surface and the ionosphere excited by lightning [95, 96]. These resonances are also monitored with sensitive magnetometers, with the future goal of subtracting
their effect on gravitational-wave strain data [97]. The effect of Schumann resonances on the
measured gravitational-wave strain is below the current Advanced LIGO–Advanced Virgo
noise floor [98].
7. Noise model and likelihood
The likelihood that the gravitational-wave strain data contains a given signal is the central
quantity in both detection and parameter estimation of gravitational-wave events. In this section we relate this likelihood to the model assumptions commonly made for the noise components of gravitational-wave detector strain data. The data time series d collected from an
interferometer can be written as the sum of the gravitational wave response of the detector, h,
and the combination of all the noise sources in that detector n such that d = n + h. Since the
true gravitational-wave signal in the detector h is unknown, we resort to using signal models
denoted by h . We consider a model h to be a good description of the signal in the data if the
residuals r = d − h are consistent with our model for the instrument noise. More quantitatively, the likelihood that the data d contains a possible signal h is given by the probability that
r is a realization of the noise model. In other words, the likelihood function is the noise model.
For Gaussian noise the likelihood can be written:
p(d|h) =

1 2
1
e− 2 χ (d,h) ,
det(2πC)1/2

(6)

where C is the noise correlation matrix, and
−1
χ2 (d, h) = r · C−1 · r = (dIk − hIk )C(Ik)(Jm)
(dJm − hJm ) .

(7)

The repeated indices include a sum over the network of detectors I, J and the data samples k
I
and m. If the noise is uncorrelated between detectors C(Ik)(Jm) = δIJ Skm
, where S is the noise
spectral density. Moreover, if the noise is stationary—so that correlations depend on only the
time lag between data samples—then the noise correlation matrix in each detector will be
I
diagonal in the Fourier domain: Skm
= δkm SI ( fk ). In that case we have χ2 (d, h) = (r|r) where
(a|b) is the familiar noise-weighted inner product:
∫ ∞
ã( f )b̃∗ ( f ) + ã∗ ( f )b̃( f )
df .
(a|b) = 2
(8)
Sn ( f )
0
The likelihood function (6) is central to Bayesian inference [99], and with the specification of
priors [100] for the signal and noise models, allows for the calculation of the model evidence
[101, 102]—giving the odds that a signal is present—and posterior distributions for the model
29

## PDF page 31

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

parameters, θ , such as the masses and spins of a binary system [103–105]. For stationary,
Gaussian noise that is uncorrelated between detectors, the likelihood function takes the form
(
[
])
∫
1∑
I
p(d|θ) = exp −
(dI − hI (θ)|dI − hI (θ)) + ln(Sn ( f )) df
,
2 I
(9)
where the sum is taken over the detectors in the network and (a|b) is the noise weighted inner
product defined in equation (8).
The likelihood function can also be used to define a frequentist detection statistic [53, 106]
given by the likelihood ratio between a signal h being present or absent in the data. If the data
were stationary and Gaussian this statistic would follow a known distribution and the false
alarm rate for an event could be computed analytically. In practice the noise exhibits deviations from stationarity and Gaussianity, and the methods used to detect and characterize signals have to be modified. Robust search methods have been developed that take into account
the measured properties of the noise. These are described in section 8. The noise modeling and
consistency checks applied to signal characterization and parameters estimation are described
in section 9.
8. Signal detection
In this section we describe how candidate signals are identified in LIGO–Virgo data and how
the statistical significance of each candidate is quantified by comparison with the observed
properties of the detector noise.
8.1. Model comparison and the matched filter

The LVC searches for gravitational waves compare the null hypothesis, H0, that a given stretch
of data contains only noise, to the signal hypothesis, H1, that the stretch of data contains both
noise and a gravitational-wave signal184. Most searches assume that general relativity correctly describes the gravitational-wave signals. The likelihood of observing the data under the
two hypotheses can be written in terms of equation (6) by
p(d | H0 ) = p0 (d)

and p(d | H1 ) = p1 (d)

(10)

where H0 assumes noise alone with no signal in the data, while H1 assumes a signal parameterized by θ , h(θ) is present in addition to the noise. For the present, we will assume that
each detector data stream is being analyzed independently, and we discuss below how data
from multiple detectors is combined in LVC searches. The probability of the signal hypothesis
given the observed data, known as the posterior probability, is given by Bayes’ theorem as
[
]−1
p1 (d) p1 (d) p(H0 )
p(H1 ) p1 (d)
p(H1 | d) =
=
+
p(H0 ) p0 (d) + p(H1 ) p1 (d)
p0 (d) p0 (d) p(H1 )
(11)
where p(H0 ) and p(H1 ) are our prior beliefs of whether a signal is absent or present in the
data. Regardless of these prior beliefs, the posterior probability is seen to be monotonic in the
likelihood ratio

184
In reality all LIGO–Virgo data may contain some level of gravitational-wave signal, but a signal can only be
detected if the null hypothesis is sufficiently disfavored relative to the signal hypothesis.

30

## PDF page 32

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Λ(d|θ) =

p(d | H1 )
p1 (d)
=
p(d | H0 )
p0 (d)

(12)

and so this quantity is the optimal test statistic [54]. For Gaussian noise, the log of the likelihood ratio can be written in terms of the inner product of equation (8) as
1
log Λ(d|θ) = (d | h(θ)) − (h(θ) | h(θ)) .
2

(13)

Only the first term of this expression involves the data; it is then observed that the posterior
probability is a monotonic function of (d | h(θ)), a quantity known as the matched filter,
which, therefore, is also an optimal test statistic.
8.2. Signal-to-noise ratio and template banks

In a matched-filter search for gravitational-wave signals, the signal parameters θ will not be
known in advance. The optimal detection statistic would be obtained by marginalizing [107]
the likelihood ratio Λ(d|θ) over all unknown parameters by integrating the likelihood ratio
over these parameters185.
Since the log likelihood ratio is a linear function of the signal model, its exponential—the
likelihood ratio itself—will generally be sharply peaked about its maximum, thus the maximum value of Λ(d|θ) over unknown parameters θ is expected to be a good approximation
to the marginalized likelihood ratio (up to a possible constant rescaling). This maximization
procedure is equivalent to minimizing the residuals seen in the detector, which can be seen as
follows. The log likelihood can be written as
1
1
log Λ(d|θ) = − (d − h(θ) | (d − h(θ)) + (d | d).
2
2

(14)

Now it is clear that the parameters θ̂ that maximize the log likelihood ratio are those that minimize the residuals d − h(θ) in terms of the noise weighted inner product.
The parameters θ describing the strain observed in a detector include the signal amplitude
A observed in the detector (which is inversely proportional to the distance to a gravitationalwave source), the phase φ of the sinusoidally-varying signal observed in the detector, the
arrival time t of the signal (usually defined by the moment when it reaches peak gravitationalwave amplitude at the detector), and other parameters µ describing the physical parameters of
the source such as the masses and spins of the components. We write
h(θ) = Ap(t, µ) cos φ + Aq(t, µ) sin φ

(15)

where p(t, µ) and q(t, µ) are in-phase (cosine) and quadrature-phase (sine) waveforms, normalized so that (p | p) = (q | q) = 1, and which are orthogonal, (p | q) = 0 .
Maximization over the amplitude and phase can be done algebraically as follows: equation (13) can be rewritten using equation (15) as
1
log Λ(d|θ) = Aρ(t, µ) cos(φ − ϕ) − A2
2

185

(16)

The integration measure to obtain an optimal statistic is given by the probability density of gravitational-wave
signals over the unknown parameters [108]: for example if the parameters θ include ι , the inclination of the binary
orbit relative to the line of sight for a compact binary gravitational-wave source, the signal probability density over
ι is uniform in cos ι [109].
31

## PDF page 33

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

where
ϕ ≡ arctan

(d | q(t, µ))
(d | p(t, µ))

(17)

and
ρ(t, µ) ≡

√
(d | p(t, µ))2 + (d | q(t, µ))2

(18)

is the SNR time series for waveform templates with parameters µ. The log-likelihood log Λ is
maximal for amplitude Â = ρ and phase φ̂ = ϕ with
max log Λ(θ) ≡ log Λ(t, Â, φ̂, µ) =
A,φ

1 2
ρ (t, µ) .
2

(19)

Peaks in this time series correspond to times at which a signal is most likely to be present.
Under the signal (noise) hypothesis, and in the presence of stationary and Gaussian noise with
a known power spectrum, ρ2 (tpeak , µ) follows a non-central (central) chi-squared distribution
with two degrees of freedom.
The SNR time series can be conveniently expressed in terms of a complex time series as
equation (8) of [66]
∫ ∞
d̃( f )p̃∗ ( f , µ) 2πift
e df
z(t, µ) = 4
(20)
Sn ( f )
0
as ρ = |z| and the phase ϕ = arg(z); p̃( f , µ) is the Fourier transform of the in-phase waveform (see equation 15). Equation (20) is the inverse Fourier transform of
z̃( f , µ) = 4

d̃( f )p̃∗ ( f , µ)
Θ( f )
Sn ( f )

(21)

where Θ( f ) is the Heaviside step function.
Parameters such as the masses and spins of the binary components (represented by µ)
change the morphology of the gravitational wave. In order to detect signals with a wide range
of possible masses and spins, a bank consisting of large numbers of signal templates spanning
the parameter space is produced, and each template in the bank is used as a matched filter.
The template bank used to initially find signals in the data is constructed with a density in
parameter space sufficiently high that the loss in SNR between a true signal and the best-fit
template is less than 3%. See [2, 3, 110] for more details on the template banks used for the
O1 and O2 searches.
An important property of the SNR should be noted: in equation (20) it can be seen that the
integrand is proportional to d̃( f )/Sn ( f ), so the data are not simply being whitened (which
would have been the case if the denominator were S1/2(f )), but in fact noisier parts of the frequency spectrum (including narrow lines) are suppressed in the matched filter. Equivalently,
the SNR integral can be seen as correlating a whitened data time series with a whitened template. The SNR therefore provides a natural way to down-weight the frequency bands where
the noise is large, and effectively notches out the various lines.
8.3. Rejection of noise artifacts and construction of candidate ranking statistic

While the SNR is the optimal detection statistic in the case of stationary Gaussian noise, transient instrumental artifacts make it a non-optimal statistic with real detector noise. Although
the matched filter naturally suppresses stationary noisy features in the data, glitches can cause
32

## PDF page 34

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

certain templates to produce high SNR values [50, 111–113]. We address this in several different ways:
(i) As explained in section 6.2, we use witness sensors to identify times when the environment
or the instrument introduces frequent glitches and we veto a subset of these times found
to impact search performance from our analysis [50]. These sensors include those that
monitor the physical environment about the gravitational-wave detector, as well as those
that record signals from within the internal control systems of the interferometer.
(ii) We implement waveform consistency tests which characterize the deviation of the data d
from the model n + h [20, 21, 66, 114]. For signals from compact binary mergers, these
tests are extremely powerful and allow us to reject many glitches which have not been
identified and vetoed, though for short signals the discriminatory power of these tests is
diminished [3, 20, 114, 115]. The exact implementation of these signal consistency tests
vary among search pipelines, but all are based on the following principle: if the gravitational-wave model waveform is subtracted from the data to produce residuals d − h , the
residuals should be consistent with Gaussian noise if the signal hypothesis is true. These
residuals are re-filtered with the matched filter over different time or frequency intervals
to determine if non-noise-like features persist; evidence of such features suggest that the
model waveform h is not a good match to the non-Gaussian feature in the data, and the
detection ranking statistic is down-weighted accordingly. For example, the consistency
test described in [66, 114] constructs a chi-squared test statistic by dividing the matched
filter into n frequency bands as
χ2 =

n
∑
|(d − h | p)i − (d − h | p)/n|2 + |(d − h | q)i − (d − h | q)/n|2

1/n

i=1

(22)
where (a | b)i is the same as the inner product in equation (8) but with the integrand
restricted to the frequency interval fi−1 < f < fi with f 0 = 0 and fn = ∞. Here the bands
are chosen so that (p | p)i = (q | q)i = 1/n . If the residual d − h is Gaussian noise, χ2
is chi-squared distributed with ν = 2n − 2 degrees of freedom; values of χ2 ≫ ν are
indicative of residual non-Gaussian features in the data after the model has been subtracted. A re-weighted ranking statistic proposed in [20]
{
1
χ2 ⩽ ν
ρ̂ = ρ × [ 1 1 2 3 ]−1/6
(23)
χ2 > ν
2 + 2 (χ /ν)

down-weights the SNR for large values of χ2. A similar time-domain based signal consistency test is described in [21] and is incorporated into a likelihood ranking statistic.
(iii) For all detections published to date we have required that gravitational-wave signals
be identified via matched filtering in at least two independent detectors with consistent
parameters. For example, the arrival times of the gravitational waves at each detector
must differ by no more than the the maximum time-of-flight between the detectors, e.g.
10 ms for the LIGO Hanford–LIGO Livingston pair, with an extra 5 ms added in order to
account for uncertainty in the inferred coalescence time at each detector. This 5 ms addition to the coincidence window is also used when searching for simultaneous events for
the LIGO Hanford–Virgo pair (27 ms light travel time), and the LIGO Livingston–Virgo
pair (26 ms light travel time) [3]. However, having now established the existence and
frequency of gravitational-wave signals, it may now also be possible to make detections

33

## PDF page 35

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

when only one detector is operating, and thus this time coincidence test is not available
[116].
The matched-filter based searches employed by the LVC construct ranking statistics from
the SNR and the waveform consistency test statistics [3]. In addition an astrophysical signal
received in several detectors will have a common set of parameters µ (within limits imposed
by limited SNR) in all detectors, and, furthermore, the amplitude, phase, and time-of-arrival
of the signals observed in each detector will be determined by the direction of propagation
of the wave (i.e. from where on the sky the signal originates) and the polarization state of the
signal. Since gravitational waves have two polarizations (in general relativity), referred to as
the plus-polarization h+ and the cross-polarization h×, the strain on detector I is determined
by the detector’s antenna response patterns F+,I and F×,I by
hI (θ) = F+,I (α, δ, ψ, t)h+ (t − τI , D, ι, µ) + F×,I (α, δ, ψ, t)h× (t − τI , D, ι, µ)
(24)
where α and δ are the right ascension and declination of the source of the gravitational waves,
D is the distance to the source of the waves, ι is the inclination of the orbital plane of the
binary system (which, for circular orbits and leading order quadrupole emission, determines
the ellipticity angle), and τI = τI (α, δ, t) is the travel time of the signal from the geocenter
to the detector. Although a fully-coherent search for gravitational waves across a network of
detectors is possible, we opt instead to perform searches independently in each detector and
then demand that triggers seen in different detectors have consistent times of arrival and the
same parameters µ since this provides a powerful glitch rejection consistency test as described
above. However, further signal consistency requirements are also possible. For the leadingorder quadrupole emission from a circular binary, the ratios of the amplitudes seen in two
detectors is
‾
(
)2
│
2ι
│ 2
2 cos2 ι
+ F×,I
│ F+,I 1+cos
2
AI
(25)
=│
(
)2
⎷
AJ
1+cos2 ι
2 cos2 ι
2
+
F
F+,J
×,J
2

while the difference in arrival time is tI − tJ = τI − τJ and the difference in phase is
(
)
(
)
F×,J 2 cos ι
F×,I 2 cos ι
φI − φJ = arctan
arctan
−
.
F+,J 1 + cos2 ι
F+,I 1 + cos2 ι

(26)

It is therefore possible to include an amplitude-phase-time consistency measure in likelihoodbased ranking statistics [20, 50, 117]; this was done for the most recent searches for gravitational-wave signals in the LIGO–Virgo O1 and O2 data [3].
8.4. Background estimation and detection confidence

After the steps described above which mitigate the effects of noise transients, the probability of remaining transients occurring simultaneously (within a time window that takes into
account the maximal travel time of a signal, for example 10 ms for the two LIGO detectors)
in two detectors and producing a large joint ranking statistic value becomes extremely small.
Different searches adopt different approaches for measuring this probability as a function of
the ranking statistic [50]. The basic method is to examine the statistical properties of the nonsimultaneous transients observed in each detector and to artificially treat them as if they did
occur simultaneously.
34

## PDF page 36

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

The statistical significance of any candidate event observed in two or more detectors is
quantified by its false alarm rate, which is the expected rate of events per time due to noise
which would be assigned an equal or larger ranking statistic than the candidate. One approach
to estimating false alarm rates is to shift one detector’s data stream in time (by a time interval
larger than the maximum time-of-flight between detectors) and repeat the search. The resulting ‘time-shifted’ coincidences are then treated as a background noise sample. This is done
numerous times with different time shifts in order to obtain a probability distribution for the
joint detector ranking statistics. Each coincident trigger is assigned a false alarm rate given
by the number of background triggers with an equal or larger ranking statistic, divided by
the total time searched for time-shifted coincidences. For example, in [1] it is found that the
frequency of transients producing more significant events than GW150914 is less than once
every 200 000 years in both of the matched-filter searches employed by the LVC.
Another similar approach is to accumulate single-detector triggers not having simultaneous (within the time-of-flight of gravitational waves) triggers in another detector and therefore
likely not associated with gravitational-wave signals. The distribution of the ranking statistic
under the background (noise only) hypothesis is then estimated by randomly drawing single detector triggers from the inferred single detector distributions and artificially treating
them as if they were simultaneous when constructing the ranking statistic. The significance
of an observed ranking statistic value can then be evaluated using this background distribution [21, 117]. These two independent methods of determining the significance of observed
gravitational-wave candidates have both yielded high significance for the gravitational waves
that have been identified.
Terrestrial noise sources that are potentially correlated between detectors are not taken into
account by these background estimation methods. Thus, as discussed in section 6.2 above, a
detailed examination of physical and environmental sensors which monitor such noise sources
and an assessment of their coupling to the measured gravitational-wave strain channel is carried out in order to check the validity of a detection candidate.
The LVC also performs searches of LIGO and Virgo data without specific waveform models [22, 118]. These searches first identify periods of excess power in each detector’s data
stream and then builds a detection statistic based on the cross-correlation between the data
streams. The significance of a particular detection statistic value is again assessed using time
shift analyses. In [1] it was shown that the frequency of noise transients producing more significant events than GW150914 in such a generic transient search is once every 8400 years.
The fact that multiple searches, employing different methods, all found GW150914 to be a
highly significant candidate bolsters our confidence that this event is not the product of coincident transient noise. Furthermore, the signal is well matched by the waveform predicted by
general relativity for the coalescence of a binary black hole system. Various tests performed
using the first ten binary black hole mergers detected by the LVC with high confidence have
shown no significant deviation from general relativity models [119].
8.5. Measurement of search sensitivity

A final component of a search pipeline is the determination of the sensitivity of the search to
astrophysical populations of signals. The purpose of doing so is two-fold: first, it provides a
metric by which a search can be tuned to optimize its detection efficiency for particular classes
of signals; second, it provides a means for interpreting the rate of signals detected by the pipeline to the rate at which signals are generated by the population.

35

## PDF page 37

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

The sensitivity of the search pipeline is normally measured via a Monte Carlo procedure
(see, e.g. [120]) in which simulated signals drawn from a hypothetical source population (e.g.
some distribution of binary component masses and spins, orientation angles, arrival times,
and distance) are added to real detector noise, and the search is rerun to determine the fraction
of signals from this population that are detected by the search pipeline. A simulated signal is
considered to be detected if the search pipeline produces a trigger above some chosen ranking statistic threshold. The result is represented as a time- and population-averaged spacetime
sensitivity ⟨VT⟩ for a fixed ranking statistic threshold which corresponds to a fixed false alarm
rate threshold (e.g. a threshold could be chosen to be one false alarm per century of observation). Alternatively, threshold-independent methods of astrophysical rate estimates can also
be employed [121–123].
9. Inferring waveform and physical parameters
Once a candidate gravitational-wave signal is identified, and its significance is established,
the next goal is to use the data to infer the physical parameters of the system that created the
gravitational waves [102–105, 124–127]. The detection of gravitational waves as well as the
inference of the physical parameters relies on knowledge of the generic shape of the signal one
is looking for as well as the distribution of the noise. Moreover, gravitational-wave signals are
weak, therefore uncertainties in these parameters may be large and a priori assumptions about
the typical amplitudes and phase evolution of such signals do have a significant impact on the
reconstructed waveform. For these reasons, inference of the physical parameters of the system, such as masses, spins of the merging objects, is done within the framework of Bayesian
parameter estimation. The central elements that need defining are a model M for the gravitational-wave signal that allows for the prediction of the form of the signal from the values of
the physical parameters of the system, and the so-called background or prior information I.
Given a model M that depends on a set of parameters θ , background information I, and a
set of observations (data) d , inference is done via application of Bayes’ theorem:
p(θ|d, M, I) = p(θ|M, I)

p(d|θ, M, I)
.
p(d|M, I)

(27)

The left hand side is referred to as the posterior probability density function, or simply the
posterior for θ , while the three terms on the right hand side are the prior probability density
function p(θ|M, I), the likelihood function p(d|θ, M I), given by equation (9) and the evidence,
∫
p(d|M, I) = dθ p(θ|M, I) p(d|θ, M, I).
(28)
Within the Bayesian parameter estimation framework, the inference is reduced to the calculation of the posterior for θ given the model M and the analysis assumptions I which uniquely
determine the prior distribution and the likelihood function.
9.1. Waveform models

Let us focus now on the choice of signal model M. The signal model M determines the functional form of h(t; θ) which is key to calculating the likelihood function. For definiteness,
we will concentrate on parametric forms of h(t; θ), as obtained by solving Einstein’s equations. For a discussion of non-parametric signal models see [128]. Exact analytic solutions of
Einstein’s equations are notoriously difficult to obtain; therefore data-analysis-ready models
36

## PDF page 38

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

are either based on perturbative solutions, e.g. the Taylor family of waveforms [129] or the
effective-one-body waveforms [130–134], or on hybrid/phenomenological approaches such
as the Phenom family of waveforms [135–138]. We will not discuss further the details of the
waveform models here, but we will restrict ourselves to the two main types of waveforms
employed in the original analysis of GW150914. For GW150914, the two models used in
[127] were SEOBNRv2 and IMRPhenomPv2 [127, 139]. Both waveform models are full
inspiral-merger-ringdown models that succeed in reproducing numerical waveforms, especially in the region of approximately equal mass and moderate spins magnitudes. The main
difference between the two models lays in the treatment of the spin dynamics. SEOBNRv2
models the dynamics of the component of the spin vectors along the direction of the orbital
angular momentum while IMRPhenomPv2 includes also an effective treatment of the dynamics of the in-plane components of the spins, and thus includes an approximate precessing
dynamics186. Because GW150914 was nearly a face-off system (orbital angular momentum
vector pointing away from the Earth), the LIGO instruments were not sensitive to the inplane spin components, hence the two waveform models are essentially equivalent. In [143],
the LVC has empirically shown that the inferred properties of GW150914 depend relatively
weakly on a change in the waveform model. This finding was confirmed by the analysis presented in [134] using an independent effective-one-body implementation and by [144], in
which numerical relativity solutions were directly compared with GW150914 data.
9.2. Prior distributions

The final functions necessary for the application of Bayes’ theorem, equation (27), are the
prior probability distributions for the parameters of interest. These are all the parameters necessary to completely characterise the gravitational-wave signal emitted during a coalescence
event. For quasi-circular orbits, these are:
• the component masses m1 and m2;
• the spin vectors ⃗S1 and ⃗S2 ;
• the polarisation angle ψ and the angle θjn between the total angular momentum ⃗J and the
propagation direction of the gravitational wave n̂;
• the source luminosity distance DL;
• the source right ascension α and declination δ ;
• a reference phase ϕ0 and a reference time, typically the gravitational-wave strain peak
time, t0.
The functional form of the prior distribution must be specified for all parameters. In some
cases the prior distribution is determined via invariance (symmetry) properties of the parameter space [145]; for instance, the prior for the source position DL , α, δ in the Universe is
chosen from the requirement that the number density of sources is uniform in the cosmological co-moving volume in accordance with a Friedmann–Lemaître–Robertson–Walker cosmological model. Thus, the probability p(DL , α, δ|M I) ∝ dV and for redshift z ≪ 1 reduces to
p(DL , α, δ|M I) ∝ D2L | cos(δ)|. In cases where invariance arguments do not apply, we choose
simple forms of prior distribution so that the resulting posteriors are easily interpretable.
Similar arguments determine the prior for the spin vectors ⃗S1 , ⃗S2 and orientation angles ψ, θjn
to be uniform over the azimuthal angles ranging between 0 and 2π as well as uniform in the
186

At the time of the discovery of GW150914 another precessing waveform model was available, SEOBNRv3,
which also includes in-plane spin components [140, 141]. The original analysis, however, did not include results
from this model, which were reported in [142].
37

## PDF page 39

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

cosine of the polar angles ranging between −1 and 1. Regarding the spin vector magnitudes,
several possible priors are possible, e.g. p(|⃗Si ||M, I) ∝ |⃗Si |2 or p(|⃗Si ||M, I) ∝ 1. The main
analysis of the events in the GWTC-1 catalog employed a uniform distribution over the norm
of the spin vectors. For the component masses m1 and m2, the chosen prior distribution is uniform, thus p(m1 , m2 |M I) ∝ 1, but limited from below so that m1 , m2 > 1M⊙.
9.3. Calibration uncertainties

In addition to uncertainties induced by detector noise, the accuracy and precision of our source
parameter estimates are also affected by uncertainties in the amplitude and phase response of
the detectors. For this reason, this source of uncertainty on the data is modelled and included
in the analysis. The calibration uncertainty model employed is based on empirical estimates
of the error magnitudes in both amplitude and phase in specified frequency bands [47, 74, 82].
In particular, the model assumes the value of the errors to be distributed as a Gaussian distribution with zero mean and a variance given by the empirically determined error magnitudes.
Calibration uncertainty curves are then constructed using third order spline interpolation over
the data frequency space. Typically, this introduces a total of O(10) additional parameters
per detector (half for the phase uncertainty and the other half for the amplitude), which are
sampled in concert with the physical parameters of the system. Technical details for the LVC
calibration model can be found in [146].
9.4. Numerical methods

The total number of parameters to be inferred is thus 15 for quasi-circular orbits and generic
spin vectors, and 11 for models where spins are forced to be aligned with the orbital angular
momentum. To the set of physical parameters, we must add the 10 parameters per detector
necessary to specify the calibration uncertainty model. Hence, for a typical three-detector
analysis, we sample a grand total of 45 parameters for a quasi-circular system with generic
spin orientations. Parameter spaces of such high dimensionality cannot be efficiently explored
with grid-based methods. Therefore, over many years members of the LVC developed the
LALInference stochastic sampler library [105] which implements two algorithms, a parallel tempering Markov chain Monte Carlo [147] and a nested sampling [102]. The parallel tempering Markov chain Monte Carlo is designed to generate samples from the multidimensional
posterior distribution (27), while the nested sampling instead is designed to calculate the evidence, equation (28) and generates samples from the posterior distribution as a by-product.
More details are given in [105] and references therein. Other parameter estimation pipelines
are routinely used by the LVC, such as rapidPE [148] and BILBY [149], but for the rest of the
discussion we will focus on LALinference. However, the same considerations will apply
to other Bayesian analysis methods.
9.5. Posterior distributions

The end products of the LALInference analyses are posterior samples for all parameters
that characterise the gravitational-wave waveform. Of particular interest are posteriors for
the intrinsic parameters, masses and spin vectors, which help ascertain the nature of the
coalescing objects. For GW150914, the detector-frame masses (i.e. redshifted due to cosmological expansion) measured using the IMRPhenomPv2 waveform model were 38.5+5.6
−3.6 M⊙
and 32.2+3.6
;
see
table
I
in
[127].
The
quoted
numbers
are
an
extremely
concise
way
−4.8 M⊙
38

## PDF page 40

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 13. One- and two-dimensional posterior distribution for the detector-frame
masses for the GW150914 event obtained using the IMRPhenomPv2 waveform model.
The three panels show (i) the one-dimensional marginal posterior for m1 (top panel);
(ii) the joint two-dimensional m1 − m2 posterior (bottom left); (iii) the one-dimensional
marginal posterior for m2 (bottom right). Posterior samples taken from [150].

of summarising the full posterior distribution. The output of LALInference analyses are
samples from the full posterior distribution. In particular, a number such as 38.5+5.6
comes
−3.6 M⊙
from the marginalisation over 14 of the 15 physical source parameters of the full posterior, as
well as the calibration parameters, to obtain a one-dimensional posterior from which the 90%
credible region is then calculated. Naturally, correlations between different parameters are
invisible in a one-dimensional representation. For a clearer picture, multidimensional posterior distributions help to display the information extracted from the analysis. Figure 13 shows
the joint two-dimensional posterior distribution for the component masses m1 and m2 as an
example. In particular, the bottom left panel shows the non-negligible correlation between the
component masses.
The full details of the multi-dimensional posterior distribution can be visualised in a compact way by computing the posterior distribution over the waveform itself in the time domain.
This is done simply by computing the predicted waveform over each of the posterior samples.
Let θ i be the ith posterior sample, the corresponding waveform will be h(t; θ i ). The waveform
samples are the set {h(t; θ i )}i=1,...,N ≡ {hi }. Each of the waveform samples hi can be whitened, see section 3, and then used to compute credible intervals at every time tj at which the
original data were sampled. The result of this procedure is summarised in the presentation of
figure 6 of [127]. Figure 1 in [1] is representing a different procedure; the second row in this
figure shows a comparison between the reconstructed 90% credible region obtained by the
procedure described above, and a numerical relativity solution that, while not corresponding
39

## PDF page 41

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 14. Scalograms (or Q-scans) of the whitened data and residuals in the LIGOHanford and LIGO-Livingston detectors in 3 s of data surrounding the GW150914
event. The residuals are free of glitches or correlated power. The color scale, as
displayed by the bar on the right, corresponds to the whitened power.

to any of the computed posterior samples, is consistent with the reconstructed 90% credible
region.
9.6. Validation of source parameter estimates

The results from Bayesian inference are only as good as the models used in the analysis. If the
waveforms used in the signal model or the underlying assumptions of the noise model are inaccurate, the results will suffer from systematic bias. A multitude of tests are used to check for
possible mis-modeling error and to quantify the impact on the analyses. As discussed earlier in
section 9.1 the waveform models are compared to highly accurate numerical relativity simulations, and multiple waveform approximants are used in the analyses and cross-compared. The
difference between the results found using different waveform models provides an estimate
of the systematic error due to the signal model. The noise model can also be checked. Other
checks include adding simulated signals with similar parameters to the astrophysical events
into nearby stretches of data and checking that the parameters are properly recovered by the
parameter estimation algorithms.
Over long stretches of LIGO–Virgo data, the noise is known to be non-stationary and nonGaussian. The overall noise levels fluctuate, and there are frequent low-SNR glitches, and
less frequently high-SNR glitches, see section 5. On the other hand, the gravitational-wave
signals spend very little time in the LIGO–Virgo sensitive band—seconds or less for black
hole binaries and minutes for neutron star binaries, and over these shorter stretches of time
the noise is generally (but not always) well approximated as stationary and Gaussian. When a
significant trigger is found by the search pipelines, the first thing the analysts look at are multiresolution time-frequency scalograms of the data surrounding the trigger (known as Q-scans).
Q-scans are qualitative checks which require visual inspection [151, 152]. These scans reveal
whether there are any loud glitches in the data, as was the case with the binary neutron star
GW170817 [8]. Once the parameter estimation analyses have been run, Q-scans of the residuals are closely examined to see if any any unmodelled noise features might have affected the
analyses. Figure 14 shows Q-scans of the whitened data and residuals surrounding GPS time
1126259462. The scans of the data reveal the signal from GW150914, while the residuals after
40

## PDF page 42

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Livingston
100

10-1

10-1

10-2

10-2

10-3

10-3

10-4
4

10-4
4

3
2
1
0
-1
-2
-3
-4

3
2
1
0
-1
-2
-3
-4

Observed Quantile

PDF

Hanford
100

-4

-3

-2

-1

0
1
Quantile

2

3

4

-4

-3

-2

-1
0
1
Quantile

2

3

4

Figure 15. Histograms and quantile-quantile plots of the whitened Fourier amplitudes
of the residuals in the LIGO-Hanford and LIGO-Livingston detectors for 4 s of data
surrounding GW150914. The shaded band in the upper panels indicates the expected
3-sigma variance from having a finite number of samples. The residuals show no
evidence of non-Gaussianity.

subtracting the maximum likelihood waveform from the parameter estimation studies [127]
show no visible evidence of glitches or correlated signal power.
In addition to these qualitative checks, more rigorous quantitative checks can be applied.
One test that is routinely applied is to reanalyze the residuals using the wavelet-based
BayesWave algorithm [128] which is able to identify any glitches and remaining coherent
power. Coherent power in the residuals could be evidence of departures from general relativity, or evidence of shortcomings in the template models or the noise model used for parameter
estimation. No significant coherent power was found in the residuals for any of the detected
events. In the case of GW150914 the lack of a coherent residual was used to place interesting bounds on possible departures from general relativity [153]. In the case of the binary
neutron star merger GW170817 [8], a loud incoherent glitch was seen to overlap the signal
in the Livingston detector. The glitch was reconstructed and removed using the BayesWave
algorithm. The glitch removal procedure has been shown to be safe in a study that injected
simulated neutron star merger signals into data with similar loud glitches, followed by removing the glitches with BayesWave and accurately recovering the true signal parameters with the
LVC parameter estimation algorithms [154].
Figure 15 shows histograms of the whitened Fourier amplitudes of the residuals in the
LIGO-Hanford and LIGO-Livingston detectors following the removal of the maximum likelihood waveform for GW150914. The residuals are taken from the parameter estimation
analysis published at the time of the discovery [127]. These residuals were used to test for
residual coherent power, which can be framed as a test of general relativity if we assume the
template to be a sufficiently accurate solution of the theory. Applying the Anderson–Darling
test of normality to the residuals yields p-values of 0.15 for LIGO-Hanford and 0.11 for

41

## PDF page 43

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

LIGO-Livingston, indicating that the residuals are consistent with the Gaussian noise model
used to define the likelihood.
Even if the residuals had failed the formal tests of stationarity and Gaussianity discussed
here, it would not necessarily imply that the parameter estimation would be strongly biased.
When the noise deviates from the model the analysis will suffer systematic bias. But for this
bias to be significant it has to be large compared to the statistical spread in the posterior distributions. Extensive studies using simulated signals added to real LIGO–Virgo data have shown
that systematic errors due to deviations from the noise models are generally negligible compared to the statistical uncertainties [104, 143, 154–157]. One exception is when the simulated
signals cover or overlap the times of glitches, in which case the biases can be large [158].
When glitches are present, tools such as BayesWave need to be used to model and remove the
glitches, ideally in concert with the parameter estimation.
9.7. Parameter degeneracies and credible intervals

Gravitational-wave templates exhibit a variety of parameter degeneracies whereby templates
with different parameters can have very similar amplitude and phase evolution, and yield very
similar likelihoods. One example of such a degeneracy is evident in the posterior distribution
for the component masses of GW150914 shown in figure 13. The degree of similarity between
templates with parameters λ, θ is measured by the match
M(λ, θ) = √

(h(λ)|h(θ))
(h(λ)|h(λ))(h(θ)|h(θ))

.

(29)

If the true signal is described by h(λ), then the expectation value of the log likelihood for
template h(θ), maximized over amplitude is
E[ln Λ(λ|θ)] =

1 2
M (λ, θ) SNR2 ,
2

(30)

where SNR is the optimal signal-to-noise ratio [159]. We see that signals that have similar
morphology, as measured by the match, yield similar likelihoods. Now suppose we hold one
parameter, θk fixed, then maximize the likelihood with respect to all the other parameters. Up
to an overall constant, we have [159, 160]
SNR2 2 k
(31)
FF (θ̄ ) ,
2
where FF(θ̄k ) is the fitting factor, or maximized match, between waveforms with θk = θ̄k and
the maximum likelihood waveform. Figure 16 compares the maximum likelihood as a function of the primary detector-frame mass for GW150914 to the fitting factor. The fitting factor
as a function of m1 was computed by maximizing the match between the overall maximum
likelihood waveform and waveforms with fixed m1. Note that the posterior distribution for this
event had a 90% credible interval of m1 = 38.5+5.6
, but templates with primary masses
−3.6 M⊙
outside this interval continue to yield large fitting factors because other parameters can be
adjusted to partly compensate the effects of the change in primary mass on the waveform. For
example, we find a fitting factor between the maximum likelihood template for GW150914
and a template with a primary mass of m1 = 70 M⊙ of FF = 0.95.
The possibility of achieving high matches, or correlations, between templates with large
primary masses and the maximum likelihood template have been cited as evidence that the
LIGO–Virgo parameter estimation analysis for GW150914 and other systems may be flawed
ln Λ(d|θ̄k ) ≡ maxj̸=k ln Λ(d|θ j ) ≃

42

## PDF page 44

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 16. The likelihood (in blue) and the fitting factor (in red) as a function of
the detector-frame primary mass m1 for GW150914. The dashed blue line shows
the estimate of the likelihood in terms of the fitting factor from equation (31). The
likelihood is scaled relative to the maximum likelihood value. The maximization was
performed over the secondary mass, spins and extrinsic parameters.

[43]. It was further hypothesized that the credible intervals were underestimated due to the
instrument noise not conforming to the likelihood model [43]. However, our confidence in
the reconstructed credible regions comes from extensive simulations designed to compare the
cumulative distributions of simulated populations against the cumulative distribution of reconstructed credible regions. The agreement between the two, see for instance figure 10 in [105],
demonstrates that our algorithms are properly computing the credible intervals. Moreover, as
we have shown, the noise properties for GW150914 are compatible with the likelihood model
used in the parameter estimation studies, further reinforcing our confidence in the method
used to compute the credible intervals.
There is no contradiction in having templates with parameters outside the quoted credible
regions producing large fitting factors with the best fit model, since even small template mismatches come with a large penalty for high signal-to-noise ratio systems such as GW150914.
For example, the difference in log likelihood between the signal with m1 = 70 M⊙ and the
global maximum is ∆ ln Λ = −32, which is what we expect to see for a SNR ≃ 25 signal
and a template with a fitting factor of FF = 0.95. But the relative likelihood for the higher
mass solution is e∆ ln Λ = 10−13.9, thus while templates with large primary masses can produce relatively good matches to the data, the probability that the primary mass is this high is
vanishingly small.
10. Residuals analysis of LIGO data around GW150914
The notion of a residual—the data minus the model—plays an important role in gravitationalwave data analysis. If the signal model matches well the true signal, then the residual should
be consistent with a draw from the noise model p(n), the probability distribution for the noise.
43

## PDF page 45

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

After known sources of correlation with independent witnesses are removed, we expect the
instrument noise in the widely separated LIGO–Virgo detectors to be fully independent, and
therefore the residuals in each detector to be uncorrelated. In contrast, gravitational-wave
signals will excite a coherent response across the network of detectors, and this difference in
correlation properties is one of the ways we are able to separate signals from noise.
As noted in section 6, it is possible to have correlated transient noise due to lightning
[92], but monitoring with magnetometers is presently adequate to rule that out as the cause
of events like GW150914 [48]. Low-level correlated magnetic noise is more of a concern
for the search for a stochastic gravitational-wave background [95–97, 161]. Seismic noise is
similarly monitored. Since the LIGO detectors share the same design and similar equipment,
the frequencies associated with synchronized clocks (GPS), electrical power (60 Hz), and
instrument resonances are monitored and suppressed in stochastic background and continuous-wave gravitational wave searches [49].
In this section we will use the data surrounding GW150914 to illustrate the discussion, but
the same considerations apply in general, and analyses of the residuals have been reported for
all significant events [119].
10.1.Signal and template comparisons

As introduced above, the physical parameters of the signal θ determine the shape and amplitude of the gravitational-wave signal h(t; θ). Numerical relativity simulations can be used
to generate reference templates [24] using intrinsic parameters taken from the Bayesian
parameter estimation studies. However, the templates still need to be projected onto the
detectors using an appropriate set of extrinsic parameters. In a single detector the projection is equivalent to time shifting, phase shifting and rescaling the reference template:
h̃(α, δt, δφ)( f ) = α h̃ref ( f )e2πif δt+iδφ.
Figure 17 shows the reference numerical relativity template from figure 2 of the GW150914
discovery paper [1] along with maximum likelihood projections onto each detector. A smooth
taper has been applied to the start of the template to avoid spectral leakage when transforming
to the Fourier domain. The data file for the template was taken from the original posting at the
GWOSC [162] and originates from the simulation SXS:BBH:0305, calculated for a system
with a mass ratio of q = 0.819, spins aligned with the orbital angular momentum with dimensionless magnitudes χ1 = 0.330 and χ2 = −0.440, and detector-frame total mass scaled to
M = 74.6M⊙. These waveform parameters are consistent with those eventually determined for
GW150914, within uncertainties, but do not exactly maximize the likelihood globally. Using
the maximization procedure described in section 8 one finds that the signal arrived at the LIGOLivingston detector 7.08 ms before the LIGO-Hanford detector, had a larger amplitude projected onto the antenna response pattern in LIGO-Hanford by a factor of 1.24, and had a phase
difference of −2.9 radians. These are, however, based on finding maximum-likelihood matches
to the detector data individually with a fixed waveform without constraining them to be consistent (for example, the relative time shift could in principle be greater than the maximum light
travel time between the detectors), a simplified procedure compared to the simultaneous multidetector likelihood maximization described in section 9. When a loud signal is present in the
data the individual and joint maximization techniques yield consistent results.
In figure 1 of the GW150914 discovery paper [1] the LIGO-Hanford data were inverted
(corresponding to a phase shift of ±π) and overlaid on the LIGO-Livingston data to illustrate
the similarity of the signals in the two detectors with minimal processing of the raw data.
In addition, the reference numerical relativity template described above was approximately
44

## PDF page 46

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Reference Template

h(t)

1
0
-1
1x10-21

Hanford

h(t)

5x10-22
0
-5x10-22
-1x10-21
1x10-21

Livingston

h(t)

5x10-22
0
-5x10-22
-1x10-21
0.2

0.25

0.3

0.35
t (s)

0.4

0.45

0.5

Figure 17. The reference numerical relativity template provided by the GWOSC [162]
for GW150914 is shown in the upper panel. The lower panels show the time, amplitude
and phase shifted versions of the template that maximize the likelihood in each LIGO
detector individually.

matched to the LIGO-Hanford and LIGO-Livingston data by adjusting the relative phase,
amplitude and time offset. These adjusted templates for each detector were passed through
the same bandpass and notch (band-reject) filters as the data and were then subtracted to produce the residuals plotted in the third row of figure 1 in that paper. Because those ‘Fig 1 PRL’
residuals were not globally optimized and were calculated from filtered data, they produce a
somewhat different result than minimizing the residuals in the whitened and bandpassed data,
as we will see below.
Figure 18 compares the whitened data to the whitened numerical relativity templates, maximized over arrival time, amplitude and phase, in the LIGO-Hanford and LIGO-Livingston
detectors. Also shown are the residuals produced by subtracting the templates from the data.
Prior to the publication of the GW150914 discovery paper [1], multiple tests were applied to
the residuals to verify they were consistent with noise. The whitened residuals in each detector were found to be consistent with a Gaussian distribution: the Fourier amplitudes pass the
Anderson–Darling test (see figure 15 in section 9), and the Fourier phases were found to be
randomly distributed. The residuals from Bayesian parameter estimation studies [127] were
analyzed using a wavelet reconstruction algorithm [128] that is able to detect coherent signals
of general morphology. The degree of coherence in the GW150914 residuals was found to be
entirely consistent with noise [153].

45

## PDF page 47

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 18. The upper panels show the whitened and bandpassed data in the LIGO-

Hanford and LIGO-Livingston detectors relative to GPS time 1126259462. The
maximum likelihood whitened templates have been superimposed on the data. The
lower panels show the residuals that are produced by subtracting the templates from
the data.
10.2.Correlation analyses

A simpler, though less sensitive, test for coherence is to cross-correlate the data in the two
detectors. The cross-correlation can be computed either in the time domain or the frequency
domain using the whitened residuals. The correlation in the time domain is defined as:
∫
H(t − τ )L(t)dt
(32)
C(τ ) = √∫
,
∫
H 2 (t)dt L2 (t)dt
where H(t) and L(t) represent the data streams from LIGO-Hanford and LIGO-Livingston
respectively. When working with a finite data segment of duration T the data may be taken
to be periodic: H(t) = H(t + T). The correlation measure is very sensitive to the positioning and duration of the time window and the bandpass filtering that is applied to the data. To
make meaningful statements about the significance of the correlation we need to know the
46

## PDF page 48

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 19. Correlations between the LIGO-Hanford and LIGO-Livingston detector
data using the same four time intervals used in the analysis in [42]. One time interval
covers the full 0.2 s of data shown in figure 18, and two others cover the first and last 0.1
s of the data. In addition, a very short time interval of duration 40 ms was selected that
covers the peak of the signal. A time lag of 7 ms is highlighted as a dotted vertical line.
The upper panel uses the filtered data from figure 1 of the GW150914 discovery paper
[1], while the lower panel uses the whitened data shown in figure 18.

distribution of the correlation measure for uncorrelated white noise, and these distributions
change depending on the duration and bandpass. When applied to uncorrelated, unit variance
Gaussian noise, the correlation coefficients follow a zero mean Gaussian distribution with a
variance that depends on the duration and bandpass. Following [42] we apply the correlation
analysis to four different time windows. The standard deviations for white Gaussian noise are
σ = 0.0870 for the 0.2 s segment, σ = 0.121 for either 0.1 s segment and σ = 0.193 for the
40 ms segment.
Figure 19 shows the correlations using the whitened data shown in figure 18 (bottom
panel), and in addition, the bandpass/notch-filtered data used to produce the panels in figure 1
of the GW150914 discovery paper [1] (top panel). There is a clear anti-correlation peak in the
LIGO-Hanford—LIGO-Livingston data at a time lag of ∼7.3 ms, which is consistent with the
time delay inferred for the gravitational-wave signal.
In contrast, figure 20 shows the correlations in the residuals produced using the procedure
described above. The residuals from figure 18 show no notable anti-correlation at ∼7 ms (bottom panel), while those from figure 1 of the GW150914 discovery paper [1] have a slight dip
at this time lag (top panel), reflecting the fact that the reference waveform used for illustration
in that paper was not the maximum likelihood waveform. For the shortest integration interval,
the residuals from figure 1 of the GW150914 discovery paper have a ∼3 sigma anti-correlation at a time lag of ∼7.45 ms, which while marginally consistent with noise, is evidence that
the signal subtraction was imperfect. In contrast, the residuals produced using the amplitude/
time/phase maximized NR waveforms and whitened data show no significant excursions, and
47

## PDF page 49

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 20. Correlations between the LIGO-Hanford and LIGO-Livingston residuals
using the same four time intervals as figure 19. The upper panel uses the residuals
shown in figure 1 of the GW150914 discovery paper [1], while the lower panel uses
the whitened residual time series shown in figure 18. The whitened residuals from the
maximum likelihood signal subtraction show no significant correlations at any time lag
for any of the time windows.

are fully consistent with noise. This is also the case for the residuals from the Bayesian parameter estimation described in section 9. Independent analyses of the GW150914 data have also
found no significant correlations between the residuals in the Hanford and Livingston detectors [32, 33].
11. Conclusions
In this article we presented a description of the properties of data from the LIGO and Virgo
detectors, and an overview of the analysis methods used by the LVC in identifying and characterizing gravitational-wave signals from the coalescence of binary black hole and binary
neutron star systems. We have especially looked closely at the data surrounding the first detection, GW150914 [1, 3, 163]. Contrary to the claims made in [42], there are no anomalous or
unexpected correlations to be seen in association with the observed gravitational-wave events
[119], including GW150914 [163]. Other analyses by independent researchers have come to
similar conclusions about the correctness of the LIGO–Virgo results [32–34, 39].
Proper handling of the LIGO and Virgo data is critical for conducting an analysis correctly.
As an example, in this paper we have used the whitened maximum likelihood waveforms (as
described in sections 9 and 10) for GW150914, which when subtracted from the data, produce
residuals that are consistent with Gaussian noise, and show no correlation between different detectors. If the template waveforms subtracted from the data are not sufficiently good
matches to the real gravitational-wave signal, then a remainder of that signal will survive in
the resulting residuals, which may thus exhibit nontrivial correlations.
48

## PDF page 50

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

Figure 1 of [1] was constructed to show as simply as possible that the signal is compatible
with general relativity. It does not illustrate the full LSC-Virgo statistical data analysis. The
figure was described in [1] as a visualization of the gravitational-wave signal at the LIGO
detectors and a comparison to one numerical relativity waveform which is consistent with the
gravitational-wave data. A statistical claim about the numerical relativity waveform and the
residuals of figure 1 of [1] was not intended, although unfortunately the figure may have been
interpreted in that way.
The LVC conducted extensive statistical studies of the GW150914 signal and of the surrounding noise, which are documented in [127]. Note that a whitened time series of GW150914
was presented in the parameter estimation companion paper for the discovery; see figure 6 of
[127]. Those studies, as well as the simpler investigations given here, support the interpretation that the signal is well matched by a black hole merger solution of general relativity. The
validity of this conclusion has been supported by subsequent data and analysis by the LVC
(including studies on all binary black hole produced gravitational-wave signals detected in
observing runs O1 and O2 [119]) as well as independent analyses.
The gravitational-wave data for Advanced LIGO and Advanced Virgo can be characterized as locally stationary and Gaussian, with deviations when glitches are present. The LVC
conducts extensive data quality, detector characterization, and calibration studies in order to
be confident of the reported detections [47, 48, 50, 74].
However, it is not necessary to assume that the data are stationary and Gaussian to search
for, and to detect with high confidence, gravitational waves from compact binary coalescence. Instead, LIGO–Virgo searches for gravitational waves use various methods to estimate
the false alarm rate directly from the data, for example, by introducing a relative time shift
between the detectors.
Previous studies have also demonstrated that the LVC’s parameter estimation results are
reliable [104, 143, 154–157]. The parameter estimation routines were also robust for the
gravitational waves from the binary neutron star merger GW170817 where there was a noise
glitch in the LIGO-Livingston data overlapping with the gravitational-wave signal [8, 154].
Parameter estimates obtained by researchers outside the LVC for GW170817 are comparable
with, and support the conclusions of, the LVC analyses [35–37]; these studies were made possible by the public release of the gravitational-wave data [24].
While the examples in this paper have concentrated on the events GW150914 and
GW170817, the conclusions presented have been demonstrated to be valid for the analysis
of the data containing all 11 gravitational-wave events detected by LIGO and Virgo to date
[3, 119]. As the LIGO and Virgo collaborations report more events [3, 164], independent
analyses of the data associated with these events by the broader scientific community will be
highly valuable and may well produce new insights. To this end, in this paper we have tried
to provide some guidance on the nature of LIGO and Virgo detector noise and on the extraction of gravitational-wave signals. The LVC encourages the scientific community to analyze
its data; LIGO and Virgo data will continue to be made publicly available on the GWOSC
website [24].
Acknowledgments
The authors gratefully acknowledge the support of the United States National Science
Foundation (NSF) for the construction and operation of the LIGO Laboratory and Advanced
LIGO as well as the Science and Technology Facilities Council (STFC) of the United
Kingdom, the Max-Planck-Society (MPS), and the State of Niedersachsen/Germany for
49

## PDF page 51

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

support of the construction of Advanced LIGO and construction and operation of the GEO600
detector. Additional support for Advanced LIGO was provided by the Australian Research
Council. The authors gratefully acknowledge the Italian Istituto Nazionale di Fisica Nucleare
(INFN), the French Centre National de la Recherche Scientifique (CNRS) and the Foundation
for Fundamental Research on Matter supported by the Netherlands Organisation for Scientific
Research, for the construction and operation of the Virgo detector and the creation and support of the EGO consortium. The authors also gratefully acknowledge research support from
these agencies as well as by the Council of Scientific and Industrial Research of India, the
Department of Science and Technology, India, the Science & Engineering Research Board
(SERB), India, the Ministry of Human Resource Development, India, the Spanish Agencia
Estatal de Investigación, the Vicepresidència i Conselleria d’Innovació, Recerca i Turisme
and the Conselleria d’Educació i Universitat del Govern de les Illes Balears, the Conselleria
d’Educació, Investigació, Cultura i Esport de la Generalitat Valenciana, the National Science
Centre of Poland, the Swiss National Science Foundation (SNSF), the Russian Foundation for
Basic Research, the Russian Science Foundation, the European Commission, the European
Regional Development Funds (ERDF), the Royal Society, the Scottish Funding Council, the
Scottish Universities Physics Alliance, the Hungarian Scientific Research Fund (OTKA),
the Lyon Institute of Origins (LIO), the Paris Île-de-France Region, the National Research,
Development and Innovation Office Hungary (NKFIH), the National Research Foundation
of Korea, Industry Canada and the Province of Ontario through the Ministry of Economic
Development and Innovation, the Natural Science and Engineering Research Council Canada,
the Canadian Institute for Advanced Research, the Brazilian Ministry of Science, Technology,
Innovations, and Communications, the International Center for Theoretical Physics South
American Institute for Fundamental Research (ICTP-SAIFR), the Research Grants Council
of Hong Kong, the National Natural Science Foundation of China (NSFC), the Leverhulme
Trust, the Research Corporation, the Ministry of Science and Technology (MOST), Taiwan
and the Kavli Foundation. The authors gratefully acknowledge the support of the NSF, STFC,
INFN and CNRS for provision of computational resources. This article has been assigned the
document number LIGO-P1900004.
References
[1] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. Lett.
116 061102
[2] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. D 93 122003
[3] Abbott B P et al (LIGO Scientific, Virgo) 2019 Phys. Rev. X 9 031040
[4] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. Lett.
116 241103
[5] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Phys. Rev. Lett.
118 221101
[6] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Astrophys. J. 851 L35
[7] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Phys. Rev. Lett.
119 141101
[8] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Phys. Rev. Lett.
119 161101
[9] Aasi J et al (LIGO Scientific Collaboration) 2015 Class. Quantum Grav. 32 074001
[10] Acernese F et al (Virgo Collaboration) 2015 Class. Quantum Grav. 32 024001
[11] Dooley K L et al 2016 Class. Quantum Grav. 33 075009
[12] Aso Y, Michimura Y, Somiya K, Ando M, Miyakawa O, Sekiguchi T, Tatsumi D, Yamamoto H and
The KAGRA Collaboration 2013 Phys. Rev. D 88 043007

50

## PDF page 52

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

[13] Akutsu T et al (KAGRA) 2017 The status of KAGRA underground cryogenic gravitational wave
telescope 15th Int. Conf. on Topics in Astroparticle and Underground Physics (TAUP 2017)
Sudbury (Ontario, Canada, 24–28 July 2017)
[14] Akutsu T et al (KAGRA) 2019 Class. Quantum Grav. 36 165008
[15] Unnikrishnan C S 2013 Int. J. Mod. Phys. D 22 1341010
[16] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration, Fermi GBM, INTEGRAL,
IceCube Collaboration, AstroSat Cadmium Zinc Telluride Imager Team, IPN Collaboration,
Insight-HXMT Collaboration, ANTARES Collaboration, Swift Collaboration, AGILE Team,
1M2H Team, the Dark Energy Camera GW-EM Collaboration and the DES Collaboration,
DLT40 Collaboration, GRAWITA: GRAvitational Wave Inaf TeAm, Fermi Large Area
Telescope Collaboration, ATCA: Australia Telescope Compact Array, Las Cumbres Observatory
Group, OzGrav, DWF (Deeper, Wider, Faster program), AST3, and CAASTRO Collaborations,
VINROUGE Collaboration, MASTER Collaboration, J-GEM, GROWTH, JAGWAR, CaltechNRAO, TTU-NRAO, and NuSTAR Collaborations, Pan-STARRS, MAXI Team, TZAC
Consortium, KU Collaboration, Nordic Optical Telescope, ePESSTO, GROND, Texas Tech
University, SALT Group, TOROS: Transient Robotic Observatory of the South Collaboration,
BOOTES Collaboration, MWA: Muchison Widefield Array, CALET Collaboration, IKI-GW
Follow-up Collaboration, H.E.S.S. Collaboration, LOFAR Collaboration, LWA: Long
Wavelength Array, HAWC Collaboration, Pierre Auger Collaboration, ALMA Collaboration,
Euro VLBI Team, Pi of the Sky Collaboration, Chandra Team at McGill University, DFN: Desert
Fireball Network, ATLAS, High Time Resolution Universe Survey, RIMAS and RATIR, SKA
South Africa/MeerKAT) 2017 Astrophys. J. Lett. 848 L12
[17] Goldstein A et al 2017 Astrophys. J. Lett. 848 L14
[18] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration, Fermi-GBM, INTEGRAL)
2017 Astrophys. J. Lett. 848 L13
[19] Coulter D A et al 2017 Science 358 1556–8
[20] Usman S A et al 2016 Class. Quantum Grav. 33 215004
[21] Messick C et al 2017 Phys. Rev. D 95 042001
[22] Klimenko S et al 2016 Phys. Rev. D 93 042004
[23] Vallisneri M, Kanner J, Williams R, Weinstein A and Stephens B 2015 J. Phys.: Conf. Ser.
610 012021
[24] Gravitational Wave Open Science Center 2020 https://gw-openscience.org
[25] Anderson S, Williams R and LIGO Scientific Collaboration 2017 LIGO data management plan
https://dcc.ligo.org/LIGO-M1000066/public
[26] González G, Vinet J-Y and LIGO Scientific Collaboration, Virgo Collaboration 2012 LSC and
Virgo policy on releasing gravitational wave tiggers to the public in the advanced detectors era
https://dcc.ligo.org/LIGO-M1200055/public
[27] Brady P, van den Brand J and LIGO Scientific Collaboration 2019 LIGO–Virgo observing plans
and public alerts www.ligo.org/scientists/GWEMalerts.php
[28] LIGO Scientific Collaboration and Virgo Collaboration 2017 Gravitational wave open science
center: Catalog GWTC-1 (https://doi.org/10.7935/82H3-HH23)
[29] LIGO Scientific Collaboration and Virgo Collaboration 2018 LIGO–Virgo O1 data release (https://
doi.org/10.7935/K57P8W9D)
[30] LIGO Scientific Collaboration and Virgo Collaboration 2019 LIGO–Virgo O2 data release (https://
doi.org/10.7935/CA75-FM95)
[31] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2018 Parameter estimation
sample release for GWTC-1 https://dcc.ligo.org/LIGO-P1800370/public
[32] Green M A and Moffat J W 2018 Phys. Lett. B 784 312–23
[33] Nielsen A B, Nitz A H, Capano C D and Brown D A 2019 J. Cosmol. Astropart. Phys.
JCAP02(2019)019
[34] Roulet J and Zaldarriaga M 2019 Mon. Not. R. Astron. Soc. 484 4216–29
[35] Dai L, Venumadhav T and Zackay B 2018 (arXiv:1806.08793)
[36] Radice D and Dai L 2019 Eur. Phys. J. A 55 50
[37] De S, Finstad D, Lattimer J M, Brown D A, Berger E and Biwer C M 2018 Phys. Rev. Lett.
121 091102
[38] De S, Capano C D, Biwer C M, Nitz A H and Brown D A 2019 Sci. Data 6 81
[39] Nitz A H, Capano C, Nielsen A B, Reyes S, White R, Brown D A and Krishnan B 2019 Astrophys.
J. 872 195
51

## PDF page 53

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

[40] Zackay B, Venumadhav T, Dai L, Roulet J and Zaldarriaga M 2019 Phys. Rev. D 100 023007
[41] Venumadhav T, Zackay B, Roulet J, Dai L and Zaldarriaga M 2019 (arXiv:1904.07214)
[42] Creswell J, von Hausegger S, Jackson A D, Liu H and Naselsky P 2017 J. Cosmol. Astropart. Phys.
JCAP08(2017)013
[43] Creswell J, Liu H, Jackson A D, von Hausegger S and Naselsky P 2018 J. Cosmol. Astropart. Phys.
JCAP03(2018)007
[44] Cornish N 2019 Gw-odw/data-guide-paper: published release https://zenodo.org/record/3380539
[45] Gravitational Wave Open Science Center 2020 GWOSC tutorials www.gw-openscience.org/
tutorials/
[46] Gravitational Wave Open Science Center 2020 LVC software at GWOSC www.gw-openscience.
org/software/
[47] Acernese F et al (Virgo Collaboration) 2018 Class. Quantum Grav. 35 205004
[48] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Class. Quantum Grav.
33 134001
[49] Covas P B et al 2018 Phys. Rev. D 97 082002
[50] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2018 Class. Quantum Grav.
35 065010
[51] Cabero M et al 2019 Class. Quantum Grav. 36 155010
[52] Maggiore M 2007 Gravitational Waves. Volume 1, Theory and experiments (Oxford: Oxford
University Press)
[53] Creighton J and Anderson W 2012 Gravitational-Wave Physics and Astronomy: an Introduction to
Theory, Experiment and Data Analysis (Wiley Series in Cosmology) (New York: Wiley)
[54] Jaranowski P and Królak A 2012 Living Rev. Relativ. 15 4
[55] Abbott B P et al (Virgo Collaboration, LIGO Scientific Collaboration) 2016 Phys. Rev. Lett.
116 131103
[56] Gravitational Wave Open Science Center 2019 www.gw-openscience.org/static/speclines/o2/
O2_lines_Virgo_V1.txt
[57] Cooley J and Tukey J 1965 Math. Comput. 19 297–301
[58] Brigham E O and Morrow R E 1967 IEEE Spectr. 4 63–70
[59] Rao K R, Kim D N and Hwang J J 2010 Fast Fourier Transform—Algorithms and Applications 1st
edn (Berlin: Springer)
[60] Tukey J W 1967 An introduction to the calculations of numerical spectrum analysis Analysis of
time series ed B Harris (New York: Wiley) pp 25–46
[61] Harris F J 1978 Proc. IEEE 66 51–83
[62] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. D 93 122004
Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. D 94 069903
[63] Aasi J et al (Virgo Collaboration, LIGO Scientific Collaboration) 2013 Phys. Rev. D 88 062001
[64] Littenberg T B and Cornish N J 2015 Phys. Rev. D 91 084034
[65] Welch P 1967 IEEE Trans. Audio Electroacoust. 15 70–3
[66] Allen B, Anderson W G, Brady P R, Brown D A and Creighton J D E 2012 Phys. Rev. D 85 122006
[67] Silverman R 1957 IRE Trans. Inf. Theory 3 182–7
[68] Dahlhaus R 1996 Stoch. Process. Appl. 62 139–68
[69] Akansu A N and Liu Y 1991 Opt. Eng. 30 912–20
[70] Meyer Y 1990 Ondelettes et Opérateurs: Ondelettes (Actualités Mathématiques) (Paris: Hermann)
[71] Anderson T W and Darling D A 1954 J. Am. Stat. Assoc. 49 765–9
[72] Wilson E B and Hilferty M M 1931 Proc. Natl Acad. Sci. USA 17 684–8
[73] Martynov D V et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. D
93 112004
[74] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Phys. Rev. D 95 062003
[75] Casanueva Diaz J 2017 Control of the gravitational wave interferometric detector Advanced Virgo
Theses Université Paris-Saclay https://tel.archives-ouvertes.fr/tel-01625376
[76] Robertson N A et al 2002 Class. Quantum Grav. 19 4043–58
[77] Karki S et al 2016 Rev. Sci. Instrum. 87 114503 (arXiv:1608.05055)
[78] Driggers J C et al (LIGO Scientific Collaboration) 2019 Phys. Rev. D 99 042001
[79] Cuoco E, Fabbroni L, Mazzoni M, Stanga R, Calamai G, Losurdo G and Vetrano F 2001 Class.
Quantum Grav. 18 1727–52
[80] Cuoco E, Losurdo G, Calamai G, Fabbroni L, Mazzoni M, Stanga R, Guidi G and Vetrano F 2001
Phys. Rev. D 64 122002
52

## PDF page 54

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

[81] Accadia T et al (VIRGO) 2011 Class. Quantum Grav. 28 025005
Accadia T et al (VIRGO) 2011 Class. Quantum Grav. 28 079501 (erratum)
[82] Cahillane C et al 2017 Phys. Rev. D 96 102001
[83] Viets A D et al 2018 Class. Quantum Grav. 35 095015
[84] Cirone A, Fiori I, Paoletti F, Perez M M, Rodríguez A R, Swinkels B L, Vazquez A M, Gemme G
and Chincarini A 2019 Class. Quantum Grav. 36 225004
[85] Cirone A et al 2018 Rev. Sci. Instrum. 89 114501
[86] Bonnand R, Ducrot M, Gouaty R, Marion F, Masserot A, Mours B, Pacaud E, Rolland L and
Was M 2017 Class. Quantum Grav. 34 175002
[87] Acernese F et al 2020 Astropart. Phys. 116 102386
[88] Aasi J et al (LIGO Scientific Collaboration, Virgo Collaboration) 2015 Class. Quantum Grav.
32 115012
[89] Aasi J et al (LIGO Scientific Collaboration, Virgo Collaboration) 2012 Class. Quantum Grav.
29 155002
[90] Isogai T, LIGO Scientific Collaboration and Virgo Collaboration 2010 J. Phys.: Conf. Ser.
243 012005
[91] Smith J R, Abbott T, Hirose E, Leroy N, MacLeod D, McIver J, Saulson P and Shawhan P 2011
Class. Quantum Grav. 28 235005
[92] Kowalska-Leszczynska I et al 2017 Class. Quantum Grav. 34 074002
[93] Effler A, Schofield R M S, Frolov V V, González G, Kawabe K, Smith J R, Birch J and McCarthy R
2015 Class. Quantum Grav. 32 035017
[94] Davis D, Massinger T J, Lundgren A P, Driggers J C, Urban A L and Nuttall L K 2019 Class.
Quantum Grav. 36 055011
[95] Thrane E, Christensen N and Schofield R M S 2013 Phys. Rev. D 87 123009
[96] Thrane E, Christensen N, Schofield R M S and Effler A 2014 Phys. Rev. D 90 023013
[97] Coughlin M W et al 2018 Phys. Rev. D 97 102007
[98] Abbott B P et al (LIGO Scientific, Virgo) 2019 Phys. Rev. D100 061101
[99] Gregory P 2005 Bayesian Logical Data Analysis for the Physical Sciences (New York: Cambridge
University Press)
[100] Box G and Tiao G 2011 Bayesian Inference in Statistical Analysis (Wiley Classics Library)
(New York: Wiley)
[101] Skilling J 2006 Bayesian Anal. 1 833–59
[102] Veitch J and Vecchio A 2010 Phys. Rev. D 81 062003
[103] Christensen N and Meyer R 2001 Phys. Rev. D 64 022001
[104] van der Sluys M V, Roever C, Stroeer A, Christensen N, Kalogera V, Meyer R and Vecchio A 2008
Astrophys. J. 688 L61
[105] Veitch J et al 2015 Phys. Rev. D 91 042003
[106] Finn L S 1992 Phys. Rev. D 46 5236–49
[107] Everitt B 2002 The Cambridge Dictionary of Statistics (Cambridge: Cambridge University Press)
[108] Searle A C 2008 Monte-Carlo and Bayesian techniques in gravitational wave burst data analysis
Proc., 12th Workshop on Gravitational wave data analysis (GWDAW-12) (Cambridge, USA,
13–16 December 2007)
[109] Schutz B F 2011 Class. Quantum Grav. 28 125023
[110] Abbott B P et al (Virgo Collaboration, LIGO Scientific Collaboration) 2016 Phys. Rev. X 6 041015
[111] Christensen N, Shawhan P and González G (LIGO Scientific Collaboration) 2004 Class. Quantum
Grav. 21 S1747–56
[112] Christensen N (LIGO Scientific Collaboration) 2005 Class. Quantum Grav. 22 S1059–68
[113] Christensen N 2010 Class. Quantum Grav. 27 194010
[114] Allen B 2005 Phys. Rev. D 71 062001
[115] Nitz A H 2018 Class. Quantum Grav. 35 035016
[116] Callister T A, Kanner J B, Massinger T J, Dhurandhar S and Weinstein A J 2017 Class. Quantum
Grav. 34 155007
[117] Cannon K, Hanna C and Peoples J 2015 (arXiv:1504.04632)
[118] Klimenko S, Yakushin I, Mercer A and Mitselmakher G 2008 Class. Quantum Grav. 25 114029
[119] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2019 Phys. Rev. D
100 104036
[120] Tiwari V 2018 Class. Quantum Grav. 35 145009
[121] Farr W M, Gair J R, Mandel I and Cutler C 2015 Phys. Rev. D 91 023005
53

## PDF page 55

B P Abbott et al

Class. Quantum Grav. 37 (2020) 055002

[122] Abbott B P et al (LIGO Scientific, Virgo) 2016 Astrophys. J. 833 L1
[123] Abbott B P et al (LIGO Scientific, Virgo) 2016 Astrophys. J. Suppl. 227 14
[124] Christensen N and Meyer R 1998 Phys. Rev. D 58 082001
[125] Röver C, Meyer R and Christensen N 2006 Class. Quantum Grav. 23 4895–906
[126] van der Sluys M, Raymond V, Mandel I, Röver C, Christensen N, Kalogera V, Meyer R and
Vecchio A 2008 Class. Quantum Grav. 25 184011
[127] Abbott B P et al (Virgo Collaboration, LIGO Scientific Collaboration) 2016 Phys. Rev. Lett. 116 241102
[128] Cornish N J and Littenberg T B 2015 Class. Quantum Grav. 32 135012
[129] Buonanno A, Iyer B, Ochsner E, Pan Y and Sathyaprakash B S 2009 Phys. Rev. D 80 084043
[130] Buonanno A and Damour T 1999 Phys. Rev. D 59 084006
[131] Damour T 2001 Phys. Rev. D 64 124013
[132] Taracchini A et al 2014 Phys. Rev. D 89 061502
[133] Bohé A et al 2017 Phys. Rev. D 95 044028
[134] Nagar A et al 2018 Phys. Rev. D 98 104052
[135] Ajith P et al 2011 Phys. Rev. Lett. 106 241101
[136] Hannam M, Schmidt P, Bohé A, Haegel L, Husa S, Ohme F, Pratten G and Pürrer M 2014 Phys.
Rev. Lett. 113 151101
[137] Husa S, Khan S, Hannam M, Pürrer M, Ohme F, Jimnez Forteza X and Bohé A 2016 Phys. Rev.
D 93 044006
[138] Khan S, Husa S, Hannam M, Ohme F, Pürrer M, Jimnez Forteza X and Bohé A 2016 Phys. Rev.
D 93 044007
[139] LIGO Scientific Collaboration 2018 LIGO algorithm Library—LALSuite free software (GPL)
https://lscsoft.docs.ligo.org/lalsuite/lalsimulation/index.html
[140] Pan Y, Buonanno A, Taracchini A, Kidder L E, Mrou A H, Pfeiffer H P, Scheel M A and Szilgyi B
2014 Phys. Rev. D 89 084006
[141] Babak S, Taracchini A and Buonanno A 2017 Phys. Rev. D 95 024010
[142] Abbott T D et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. X 6 041014
[143] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2017 Class. Quantum
Grav. 34 104002
[144] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration) 2016 Phys. Rev. D 94 064035
[145] Royden H and Fitzpatrick P 2017 Real Analysis (Classic Version) (Math Classics) (London: Pearson)
[146] Farr W, Farr B and Littenberg T 2015 https://dcc.ligo.org/LIGO-T1400682/public
[147] Röver C, Meyer R and Christensen N 2007 Phys. Rev. D 75 062004
[148] Lange J, O’Shaughnessy R and Rizzo M 2018 (arXiv:1805.10457)
[149] Ashton G et al 2019 Astrophys. J. Suppl. 241 27
[150] LIGO Scientific Collaboration and Virgo Collaboration 2018 O1 parameter estimation samples
release https://dcc.ligo.org/LIGO-T1800235/public
[151] Chatterji S K 2005 The search for gravitational-wave bursts in data from the second LIGO science
run PhD Thesis (Cambridge, MA: Massachusetts Institute of Technology)
[152] Zooniverse 2020 Gravity Spy www.zooniverse.org/projects/zooniverse/gravity-spy
[153] Abbott B P et al (Virgo Collaboration, LIGO Scientific Collaboration) 2016 Phys. Rev. Lett.
116 221101
[154] Pankow C et al 2018 Phys. Rev. D 98 084016
[155] Raymond V, van der Sluys M V, Mandel I, Kalogera V, Röver C and Christensen N 2010 Class.
Quantum Grav. 27 114009
[156] van der Sluys M, Mandel I, Raymond V, Kalogera V, Röver C and Christensen N 2009 Class.
Quantum Grav. 26 204010
[157] Berry C P L et al 2015 Astrophys. J. 804 114
[158] Powell J 2018 Class. Quantum Grav. 35 155017
[159] Del Pozzo W, Grover K, Mandel I and Vecchio A 2014 Class. Quantum Grav. 31 205006
[160] Cornish N, Sampson L, Yunes N and Pretorius F 2011 Phys. Rev. D 84 062003
[161] Abbott B et al (LIGO Scientific Collaboration) 2007 Astrophys. J. 659 918–30
[162] Gravitational Wave Open Science Center 2016 GW150914 SXS waveform file https://
gw-openscience.org/GW150914data/P150914/fig2-unfiltered-waveform-H.txt
[163] Gravitational Wave Open Science Center 2016 Gravitational-wave open science center release of
GW150914 (https://doi.org/10.7935/K5MW2F23)
[164] Abbott B P et al (LIGO Scientific Collaboration, Virgo Collaboration, KAGRA) 2018 Living Rev.
Relativ. 21 3
54
