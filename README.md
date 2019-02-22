# D-3_SEKURO
Tugas D-3 Programming Anggota: 16518311, 16518006, 16918226

# Platinum Rift Episode 2  
  Berupa turn based strategy game. Goals dari game ini adalah untuk menguasai seluruh wilayah tiles, termasuk menaklukan base musuh. Tampilan game tersusun dari tiles yang berbentuk hexagonal yang disimpan dalam code berupa array of array yang terhubung atau linking dengan aray yang lainnya untuk ditrack dan kemudian membentuk suatu map. Setiap start game map digenerate randomly dengan link antar tiles yang berbeda-beda.
  Game diawali dengan kedua belah pihak memiliki 10 POD/pesawat untuk menyerang. Main action dari game Platinum Rift ini adalah moving (Berpindahnya POD ke tiles lain untuk menguasai atau mengakumulasi platinum bars yang ada), buying (menambah jumlah POD dengan Platinum yang dimiliki, yaitu setiap kali melewati tile dengan PLatinum bar, maka Platinum bar akan terakumulasi menjadi uang untuk melakukan "buying" POD yang dilakukan secara otomatis. ), distributing (penggunaan PLatinum bars), fighting (perang dengan POD musuh berdasarkan jumlah POD yang dimiliki), serta owning (menguasai suatu wilayah yang dilalui atau menguasai base musuh setelah memenangi fighting). 
  
# Main Game Condition
Win Condition : 
  Menempati atau menguasai base musuh atau setelah melewati limit turn game yaitu 250 turn (per-player), winner adalah pihak dengan dominasi wilayah terbanyak.
 
Lose Condition : 
  Base yang dimainkan telah dikuasai oleh pemain musuh, atau setelah melewati turn limit yaitu 250 turn (per-player), jumlah wilayah yang dikuasai kurang dari jumlah wilayah yang dikuasai musuh. 
 
# Game Rules 
Moving :
  - Setiap POD/Grup of POD hanya dapat melakukan satu kali move atau hanya boleh berpindah tile satu kali per-turn
  - Setiap POD hanya dapat move ke tile yang telah tergenerate (yang belum teroccupied, yang telah dikuasai sendiri, ataupun yang dikuasai       oleh pemain musuh
  - Apabila terdapat tile yang sedang dalam kondisi fighting, maka POD tidak dapat masuk ke tile ini
  
Buying :
  - Automatically Done -
  
Distributing :
  - Player memperoleh jumlah Platinum bars sesuai dengan yang terakumulasi pada wilayah 
  - Bar menambah pada jumlah bar yang telah di-mine oleh player dan belum diconvert menjadi POD
  
Fighting :
  - Fighting akan berjalan apabila terdapat 2 POD dari kedua pihak lawan yang masuk ke dalam satu tile yang sama
  - Pada Fighting mode, jumlah POD yang akan hancur tiap turn adalah 3 POD dan jumlah POD yang lebih banyak akan suatu saat tetap bertahan 
    dan tidak hilang
    
Owning  :
  - Zone atau tile yang pernah dilewati oleh salah satu player akan tetap menjadi miliknya dan akan tetap menjadi milik player yang telah
    menguasainya sebelumnya.
  - Zone yang dimasuki kedu apihak player yang kemudian masuk ke mode fighting tidak akan berubah ownership dan akan tetap neutral atau 
    menjadi milik pihak yang telah menguasainya
    
# Game Modules
1. Explore
  - Mengirimkan beberapa POD untuk mengoccupy banyak wilayah
  - Mencari tiles yang memiliki Platinum Bars dan kemudian mengoccupynya
  - Mencari jalur terdekat menuju base musuh 
  
2. Offence 
  - Mendeteksi tiles wilayah player yang dioccupy oleh musuh unutk kemudian mengirim POD untuk reoccupy
  - Selalu mengirimkan POD menuju base musuh 
  
3. Defend
  - Mendeteksi apakah ada musuh pada jarak tertentu untuk kemudian mengirim POD dan mengeliminasi musuh tersebut
  - Mengirim POD ke sekitar base untuk menjadi pertahanan
 
  
  

   
  
  
