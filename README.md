# Aigaio Skytech Maps — εκδόσεις

Το αποθετήριο κρατάει **μόνο** το `latest.json`, το manifest που διαβάζει
η εφαρμογή για να δει αν υπάρχει νεότερη έκδοση. Ο πηγαίος κώδικας ΔΕΝ
βρίσκεται εδώ.

Τα αρχεία εγκατάστασης είναι στα [Releases](../../releases).

## Πώς βγαίνει νέα έκδοση

```
python bump_version.py 2.0.1        # συγχρονίζει main.py, version_info.txt, latest.json
BUILD_ALL.bat                        # παράγει installer\Output\...Setup_v2.0.1.exe
gh release create v2.0.1 <exe> --repo aigaioskytech/maps-releases
```

Το `latest.json` ανεβαίνει **τελευταίο**: αλλιώς οι πελάτες βλέπουν
αναβάθμιση που δεν έχει ακόμα αρχείο να κατεβάσουν.
