## Νικητής

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Σε αυτό το βήμα, θα εντοπίσεις τον παίκτη που φτάνει στην πλατφόρμα **Τέλος** για να κερδίσει το παιχνίδι. 
</div>
<div>
![](images/winner-aims.png){:width="300px"}
</div>
</div>

Θα προσθέσεις έναν βρόχο `για πάντα`{:class="block3control"} που ελέγχει εάν ο **χαρακτήρας** σου βρίσκεται στο επίπεδο της πλατφόρμας και αν ναι, `εάν`{:class="block3control"} έχει φτάσει στην πλατφόρμα **Τέλος**.

--- task ---

**Επίλεξε:** Πρόσθεσε έναν ήχο νίκης που ταιριάζει στον χαρακτήρα σου.

--- /task ---

###  End the game when touching a coloured platform

--- task ---

Use a `touching color`{:class="block3sensing"} block to detect when your character sprite reaches the **End** platform.


```blocks3
when I receive [start v]
forever
if <(size) = (landed)> then // not in the air
if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
stop [other scripts in sprite v] // stop jumping after win
go to (End v)
play sound (Win v) until done
stop [all v]
end
end
end
```

Το μπλοκ `σταμάτησε άλλα σενάρια σε αυτό το αντικείμενο`{:class="block3control"} σταματά τον βρόχο που κάνει τον χαρακτήρα να πηδήξει.

A `broadcast (stop v)`{:class="block3events"} message is used when your game is finished so that other sprites can stop, but this sprite can do something such as playing a sound before it stops.

--- /task ---

Use the eyedropper to pick the colour of your **End** platform

--- task ---

```blocks3
<touching color (#20f73b) ?>

```
Click on the colour input to open the colour picker and then click on the eyedropper at the bottom.

![](images/eye-dropper-tool.png)

Move the mouse pointer over to the End platform on the Stage and click to select the colour.

![](images/eye-dropper-stage.png)

The colour in the block input will change to match the colour you chose. Click in the Code area to close the colour picker.

--- /task ---

--- task ---

**Δοκιμή:** Κάνε κλικ στην πράσινη σημαία και μετακίνησε τον χαρακτήρα σου στη Σκηνή. Βεβαιωσου ότι ακούς τον ήχο νίκης όταν φτάσεις στην πλατφόρμα **Τέλος**.

**Συμβουλή:** Είναι πολύ σημαντικό να δοκιμάσεις το έργο σου πριν προχωρήσεις στο επόμενο βήμα και προσθέσεις περισσότερο κώδικα. Είναι πιο δύσκολο να βρείς και να διορθώσεις σφάλματα όταν έχεις προσθέσει περισσότερο κώδικα.

--- /task ---


--- task ---

**Εντοπισμός σφαλμάτων:**

--- collapse ---

---
title: Το αντικείμενό μου δεν πηγαίνει στο κέντρο της πλατφόρμας Τέλος
---

Πρέπει να βεβαιωθείς ότι όλες οι ενδυμασίες του αντικειμένου σου είναι κεντραρισμένες στο πρόγραμμα επεξεργασίας Ζωγραφικής.

Το μπλοκ `πήγαινε σε (άλλο αντικείμενο)`{:class="block3motion"} μετακινεί ένα αντικείμενο έτσι ώστε το κέντρο του να βρίσκεται στην ίδια θέση με το κέντρο του άλλου αντικειμένου. Εάν τα κέντρα τους βρίσκονται σε λάθος θέση, τότε ο **χαρακτήρας** σου δεν θα πάει στο κέντρο των πλατφορμών.

--- /collapse ---

--- collapse ---

---
title: Το παιχνίδι τελειώνει πολύ νωρίς
---

Βεβαιώσου ότι το αντικείμενό σου δεν αγγίζει το χρώμα του Τέλους όταν δεν βρίσκεται στην πλατφόρμα **Τέλος** — εάν χρησιμοποιείς το ίδιο χρώμα σε άλλο σημείο του έργου σου, τότε ο χαρακτήρας σου μπορεί να πεθάνει πολύ νωρίς.

--- /collapse ---

--- collapse ---

---
title: Ο ήχος δεν ακούγεται όταν προσγειώνομαι στην πλατφόρμα Τέλος
---

Κάνε κλικ στο αντικείμενο του **χαρακτήρα** και μετά στην καρτέλα 'Ήχοι'. Βεβαιώσου ότι έχεις προσθέσει τον ήχο Τέλος στο αντικείμενό σου. Κάνε κλικ στο κουμπί **Αναπαραγωγή** για να βεβαιωθείες ότι ο ήχος λειτουργεί στον υπολογιστή σου.

Κάνε κλικ στην καρτέλα **Κώδικας** και έλεγξε ότι ο σωστός ήχος βρίσκεται στο μπλοκ `παίξε ήχο`{:class="block3sound"} που εκτελείται όταν το αντικείμενο φτάσει στην πλατφόρμα **Τέλος**.

Βεβαιώσου ότι το χρώμα είναι σωστό στο μπλοκ `αγγίζει χρώμα`{:class="block3sensing"}. Επίλεξε το ξανά εάν δεν είσαι σίγουρος. Μερικές φορές τα χρώματα μοιάζουν αλλά δεν είναι ίδια.

```blocks3
when I receive [start v]
forever
if < (size) = (landed) > then // not in the air
+if <touching color (#b89d2f) ?> then // at end
broadcast (stop v) // stop other sprites
go to (End v)
+play sound (Win v) until done
stop [all v]
end
end
end
```

--- /collapse ---

Εάν έχεις κάποιο σφάλμα που δεν έχουμε καλύψει εδώ, ενημέρωσέ μας στα σχόλια. Εάν διορθώσεις μόνος/η σου το σφάλμα (μπράβο!), ενημέρωσέ μας για αυτό.

**Συμβουλή:** Εάν έχεις κολλήσει, δοκίμασε να διαβάσειςτον κώδικά σου δυνατά ή από μέσα σου για να βεβαιωθείς ότι λέει αυτό που νομίζεις ότι κάνει. Μπορεί να βρεις το σφάλμα.

--- /task ---

--- save ---
