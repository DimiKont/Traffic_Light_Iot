# Τελική Εργασία
## Στόχος

Επιβεβαίωση γνώσεων σε θέματα: μικροελεγκτών και μελέτη των πόρων του υλικού, αρχική
εγκατάσταση, δραστηριότητες σειριακής επικοινωνίας, ψηφιακές και αναλογικές είσοδοι/έξοδοι, χρήση
και συνδεσμολογία ηλεκτρονικών στοιχείων, πλατφόρμες IoT και δικτύωση υλικού, ανταλλαγή
δεδομένων μεταξύ υλικού και πλατφόρμας, μελέτη πρωτοκόλλων επικοινωνίας και διαθέσιμων APIs,
γραφική απεικόνιση δεδομένων.

## Ζητούμενα

### Α. Ηλεκτρικός φωτεινός σηματοδότης

Καλείστε να δημιουργήσετε έναν φωτεινό σηματοδότη του οποίου η λειτουργία θα ορίζεται από τον
μικροελεγκτή Arduino και θα απεικονίζεται στην πλατφόρμα IoT ThingSpeak. Ο φωτεινός σηματοδότης
θα πρέπει να λειτουργεί αδιάλειπτα, με τις εναλλαγές των ενδείξεων να ακολουθούν τη σειρά:

```
(α) Κόκκινη ένδειξη, διάρκεια >=30secs
(β) Πράσινη ένδειξη, διάρκεια >=30secs
(γ) Πορτοκαλί ένδειξη, διάρκεια >=20secs
(δ) Κόκκινη ένδειξη, διάρκεια >=30secs
(ε) ....κ.λπ.
```
Για την δραστηριότητα αυτή θα χρειαστεί να υλοποιήσετε τα ακόλουθα:

**1.** Χρήση οπτικών στοιχείων στο ThingSpeak κανάλι με σκοπό την απεικόνιση της παραπάνω επιθυμητής
    λειτουργίας. Στην Εικόνα 1 εμφανίζεται ενδεικτική περίπτωση χρήσης των οπτικών στοιχείων.
    
**2.** Σύνδεση των παραπάνω οπτικών στοιχείων με μεταβλητή ή μεταβλητές του καναλιού.

**3.** Σύνδεση του Arduino στο πλησιέστερο WiFi AP με τη χρήση του ESP-01.

**4.** Προγραμματισμός του Arduino με στόχο την λειτουργία των οπτικών στοιχείων στο ThingSpeak,
    σύμφωνα με τις παραπάνω απαιτήσεις της Δραστηριότητας.

### Β. Αποστολή δεδομένων σε κανάλι άλλης εφαρμογής

Καλείστε να ενσωματώσετε στον κώδικα του Ζητούμενου Α.4, την **δυνατότητα ορισμού τιμής για μία
μεταβλητή** , έστω την μεταβλητή Field 8 , του **καναλιού άλλης εφαρμογής** (δηλαδή καναλιού άλλου
φωτεινού σηματοδότη, άλλης ομάδας εργασίας). Για το σκοπό αυτό θα χρειαστείτε τα στοιχεία του
καναλιού της άλλης εφαρμογής, τα οποία και θα πρέπει να αναφέρετε στην υλοποίηση και στα
παραδοτέα σας. Για τον καλύτερο έλεγχο της εφαρμογής σας, οι αλλαγές που θα εφαρμόζονται στο
Field 8 του καναλιού της άλλης εφαρμογής, να εφαρμόζονται **και στο Field8 του δικού σας καναλιού σας**.

Για την συγκεκριμένη δραστηριότητα θα χρειαστεί να υλοποιήσετε:

**1.** Προγραμματιστικό κώδικα ο οποίος να υλοποιεί όσα υλοποιούσε ο κώδικας του Ζητούμενου Α.4 και
    **επιπλέον** να θέτει τιμή 0 στην μεταβλητή **Field 8 καναλιού άλλης εφαρμογής**.
    
**2.** Προγραμματιστικό κώδικα ο οποίος να υλοποιεί όσα υλοποιούσε ο κώδικας του Ζητούμενου Α.4 και
    **επιπλέον** να θέτει τιμή 0 στην μεταβλητή **Field 8 του δικού σας καναλιού**.

**ΣΗΜΕΙΩΣΗ:** Ως Field 8 αναφέρεται εδώ η μία από τις 8 μεταβλητές που παρέχονται σε ένα κανάλι
ThingSpeak. Για περισσότερες πληροφορίες, ανατρέξτε στην 2η εργαστηριακή άσκηση.

### Γ. Ανάγνωση δεδομένων σε κανάλι άλλης εφαρμογής

Καλείστε να ενσωματώσετε στον κώδικα του Ζητούμενου Β.2, την **δυνατότητα ανάγνωσης της τιμής μίας
μεταβλητής** , έστω της μεταβλητής Field 8. Η συγκεκριμένη μεταβλητή είναι ήδη καθορισμένη από τον
κώδικα του Ζητούμενου Β.2 να έχει τιμή 0. Εδώ χρησιμοποιείται η Field 8 ως μεταβλητή ειδοποίησης, η
οποία θα έχει πάντα τιμή 0. Αν και για όσο αποκτήσει τιμή 1, θα πρέπει ο φωτεινός σηματοδότης να
τίθεται προσωρινά εκτός λειτουργίας, δηλαδή να έχει πορτοκαλί φωτεινή ένδειξη.
Για την συγκεκριμένη δραστηριότητα θα χρειαστεί να υλοποιήσετε:

**1.** Προγραμματιστικό κώδικα ο οποίος να υλοποιεί όσα υλοποιούσε ο κώδικας του Ζητούμενου Β.2 και
**επιπλέον** να καθορίζει φωτεινή ένδειξη **πορτοκαλί** στην φωτεινό σηματοδότη, όταν η **Field 8**
**αποκτήσει τιμή 1** και έως ότου επανέλθει σε τιμή 0.

**2.** Προσθήκη ρύθμισης στον προγραμματιστικό κώδικα του Ζητούμενου Γ. 1 , ώστε το Field 8 να αποκτά
τιμή 1 **κάθε 10 λεπτά** και αυτό να διαρκεί **για 1 λεπτό**.

## Παραδοτέα


Για τις παραπάνω δραστηριότητες θα χρειαστεί να υποβάλετε:

**1. Αρχείο κειμένου** με: περιγραφή της εφαρμογής σας και των λειτουργιών της, απεικόνιση και
επεξήγηση του κυκλώματος υλικού, περιγραφή των ρυθμίσεων του καναλιού ThingSpeak (οπτικά
στοιχεία που χρησιμοποιήθηκαν, ρυθμίσεις μεταβλητών, κ.λπ.), ανάλυση του κώδικα που έχετε
συντάξει. Θα πρέπει το αρχείο κειμένου να εμπεριέχει ξεκάθαρη αναφορά στις επιμέρους
Δραστηριότητες.

**2. Αρχεία** *.ino με των προγραμματιστικό κώδικα των Ζητούμενων Α.4, Β.1, Β.2, Γ.1 και Γ.2.
Τα παραπάνω αρχεία θα πρέπει να υποβληθούν σε ένα συμπιεσμένο αρχείο με ενδεικτικό όνομα
αρχείου **ΑΑΑΑΑ_ΒΒΒΒΒ.zip** , όπου AAAAA και BBBBB οι ΑΜ των μελών της ομάδας εργασίας.

```
ΥΠΕΝΘΥΜΙΖΕΤΑΙ πως τα αποτελέσματα της Τελικής Εργασίας θα παρουσιαστούν από τα μέλη της
ομάδας εργασίας στον χώρο του εργαστηρίου. Η υποβολή των παραδοτέων και η παρουσίαση
απαιτούνται για την αξιολόγηση των μελών της ομάδας εργασίας. Τα παραπάνω ισχύουν και για όσους
ανήκουν στο τμήμα [overflow].
```

