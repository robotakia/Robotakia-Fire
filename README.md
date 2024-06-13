# Robotakia Fire
 Μικρό Δημοτικό - «Εντοπισμός διαδρομής Πυροσβεστικής» 

# Περιγραφή
Σε μία μακέτα που αναπαρίσταται ένα δάσος στο οποίο μόλις ξεκίνησε μία πυρκαγιά, ένα πυροσβεστικό όχημα προσπαθεί να βρει τον δρόμο του μέσα στο δάσος. Δυστυχώς ένας από τους δύο διαθέσιμους δρόμους  έχει κλείσει από την φωτιά. Ευτυχώς όμως έχουμε φτιάξει ένα σύστημα τεχνητής νοημοσύνης που επεξεργάζεται εικόνες από ψηλά και μπορεί να εντοπίσει ποιος από τους δύο δρόμους είναι ανοιχτός. Πιο συγκεκριμένα, έχοντας στήσει μία webcam πάνω από την μακέτα εκπαιδεύσαμε το teachable machine with google (https://teachablemachine.withgoogle.com/train/image) να ξεχωρίζει πότε το εμπόδιο είναι σε έναν από τους δύο δρόμους. Μέσω του προγραμματιστικού περιβάλλοντος stretch3.github.io συνδεόμαστε στο μοντέλο που εκπαιδεύσαμε μέσω της επέκτασης TM2Scratch και κατηγοριοποιείται live η εικόνα της κάμερας σε μία από τις 2 κατηγορίες, μία για κάθε δρόμο. Το πυροσβεστικό όχημα είναι το Edison και ακολουθεί μια γραμμή στο δάσος. Όταν φτάσει στη διασταύρωση ανιχνεύεται από το πρόγραμμά μας καθώς πατάει επάνω σε μια αλουμινένια πλάκα που είναι συνδεδεμένη μέσω ενός MicroBit και της επέκτασης MicroBit more στο προγραμματιστικό μας περιβάλλον. Εάν τότε έχει ανιχνευτεί εμπόδιο από την κάμερα και το Edison  πρέπει να στρίψει, δίνεται εντολή στα ηχεία να παίξουν έναν ήχο από παλαμάκια. Το Edison έχει προγραμματιστεί με iconblocks να αντιδρά στο παλαμάκι στρίβοντας, οδηγώντας το στον παράδρομο που δεν υπάρχει κάποιο εμπόδιο. 

# Εκπαιδευτικοί Στόχοι
1. Ευαισθητοποίηση των μαθητών σε περιβαλλοντικά προβλήματα και χρήση της τεχνολογίας και της τεχνητής νοημοσύνης για την αντιμετώπισή τους. 

2. Χειροτεχνία μακέτας δάσους και πυρκαγιάς που καλλιεργεί την καλλιτεχνική τους φαντασία. 

3. Κατανόηση των δυνατοτήτων, αρχών λειτουργίας και βασικής ορολογίας της Τεχνητής Νοημοσύνης. 

4. Εκπαίδευση μοντέλου Όρασης Υπολογιστών και γνωριμία με το teachable machine με σκοπό την εξερεύνηση και την εφαρμογή της τεχνητής νοημοσύνης 

5. Γνωριμία με το Edison Robot και με τον προγραμματισμό του με icon blocks. Προγραμματισμός με την εκπαιδευτική γλώσσα Scratch.Με τη δημιουργία εντολών προγραμματισμού, προωθούμε την ανάπτυξη λογικής σκέψης. 

6. Γνωριμία με το MicroBit με στόχο την εξοικείωση με νέες τεχνολογίες. 

7. Ανακάλυψη της  σύνθεσης διαφορετικών υποσυστημάτων σε ένα ενιαίο σύστημα. 

8. Ενθάρρυνση και προώθηση της συν εργατικότητας και της ομαδικότητας με σκοπό την επίλυση σύνθετων προβλημάτων. 

# Λειτουργίες και Τεχνικές
## Edison Robot
Ακολουθεί μία άσπρη γραμμή μέσα στο δάσος και όταν ακούσει το παλαμάκι στρίβει βγαίνοντας εκτός γραμμής μέχρι να βρει την άσπρη γραμμή της διακλάδωσης. Το παλαμάκι θα το ακούσει ιδανικά όταν πατήσει τον διακόπτη / πλακα που φτιάξαμε και μπροστά του έχει εντοπιστεί εμπόδιο από την κάμερα.

## Διακόπτης
Ένας διακόπτης από φύλλα αλουμινίου που δίνει σήμα στο MicroBit ότι πατήθηκε, ιδανικά από το Edison ενώ ανάβει παράλληλα ένα LEDάκι. 

## MicroBit
Λαμβάνει σήμα από τον διακόπτη ότι πατήθηκε και τροφοδοτεί το LEDάκι. Ταυτόχρονα στέλνει σήμα στον υπολογιστή όταν πατηθεί η ο διακόπτης να παίξει το ηχογραφημένο παλαμάκι από τα ηχεία αν το μοντέλο τεχνητής νοημοσύνης αναγνωρίζει ότι υπάρχει εμπόδιο.

## Scratch3
Ένα πρόγραμμα στον υπολογιστή ελέγχει το MicroBit και επικοινωνεί με τον εξυπηρετητή του Teachable Machine. Αν το MicroBit και το μοντέλο τεχνητής νοημοσύνης που εκπαιδεύσαμε δώσουν σήμα να στρίψει το Edison τότε παίζει ένα ηχογραφημένο παλαμάκι από τα ηχεία και το MicroBit στρίβει.

# Υλικά 
Ρομπότ Edison V2.0 - 54.90 € 

BBC Micro:bit V2 Board – 19.90 €

Webcam – 20 € 

USB mini cable – 5 €  

5 κροκοδειλάκια σύνδεσης - 4 €

# Επιπλέον Πληροφορίες
Δείτε την παρουσίαση του έργου μας: https://youtu.be/Vcv_YBVk7qM

Θα βρείτε τη σελίδα του έργου μας: https://openedtech.ellak.gr/robotics2024/robotakia-fire-entopismos-diadromis-pirosvestikis/ 
