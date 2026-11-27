# YaraShop — version avec page Admin (Netlify + Decap CMS)

**Chno had l version ?** Hiya nafs YaraShop li 3ndek daba (marquee, hero, categories,
l 6 produits TEST, WhatsApp), walakin l produits mab9awch maktoubin f l HTML :
kaynin f fichier `products.json`, o 3ndek page **Admin** (`/admin`) bach tzid produit,
tbeddel taman, o tmsa7 l produits TEST — bla ma tsennani.

## ⚠️ 7aja mohimma : drag-and-drop MA YKHDEMCH m3a l Admin

L Admin kay7fed l produits f GitHub (b Netlify Identity + Git Gateway).
Ila deployiti ghir b drag-and-drop (b7al l merra lli fatet), l Admin ghadi yban
walakin **ma ghadi y7fed walo** — khass l site ykoun connecté l GitHub.
Hado l steps khass **nta** dirhom (ana ma n9derch ndir compte b smiytek) :

## Les étapes (10–15 minutes)

### 1. GitHub — dir compte o repo
1. Dkhol [github.com](https://github.com/) o dir compte free (b email dyalek).
2. Dir repo jdid : **New repository** → smiya `yarashop` → **Public** → **Create repository**.
3. Uploadi **ga3 l fichiers dyal had l dossier** f l repo :
   `index.html`, `products.json`, `netlify.toml`, dossier `admin/` o dossier `images/`.
   (F GitHub : **Add file → Upload files**, o jerr l fichiers.)
   ⚠️ Khass l fichiers ykounou f l racine dyal l repo, machi f dossier wast dossier.

### 2. Netlify — connecti l repo (bla drag-and-drop)
1. F Netlify, sir l **Sites** → **Add new site → Import an existing project**.
2. Khtar **GitHub** o 3ti l permission, o khtar repo `yarashop`.
3. Build settings : **Build command : (khawi)**, **Publish directory : (khawi / racine)**.
4. **Deploy site** — ghadi y3tik lien jdid (wla ykhdem 3la nafs l site ila beddelti l settings dyalo).
5. (Optionnel) F **Site settings → Change site name**, dirha `yarashop` bach l lien ywelli `yarashop.netlify.app`.

### 3. Netlify Identity + Git Gateway — bach l Admin ykhdem
1. F Netlify, f l site dyalek : **Site configuration → Identity → Enable Identity**.
2. F nafs l page : **Identity → Services → Git Gateway → Enable Git Gateway**.
3. F **Identity → Invite users** : 3ayet l rassek b l email dyalek.
4. Fte7 l email, clique 3la l lien d'invitation, o dir l password dyalek.

### 4. Sta3mel l Admin
1. Dkhol `https://yarashop.netlify.app/admin/` (wla l lien dyal site dyalek + `/admin/`).
   Kayn ta lien **Admin** f l footer dyal l site.
2. Connecta b l email o password li derti.
3. Sir l **Produits** :
   - **Bach tmsa7 l produits TEST :** 7iyed l produits li smiytohom b `TEST - ...` (bouton 🗑️), o clique **Publish**.
   - **Bach tzid produit jdid :** clique **Add Produits**, 3emmer : ID, Nom (français), Prix (DH), Taille, Catégorie, Photo (upload), Description — o **Publish**.
4. L site kaytbeddel raso f ~1 minute (Netlify kay-redeployi).

## Chno f had l dossier ?

| Fichier | Chno howa |
|---|---|
| `index.html` | L site YaraShop (nafs l design, kayqra l produits men `products.json`) |
| `products.json` | L liste dyal l produits (6 TEST daba) |
| `admin/index.html` | Page Admin (Decap CMS) |
| `admin/config.yml` | Configuration dyal l Admin (champs dyal l produit) |
| `images/products/*.jpg` | Tsawer dyal l 6 produits TEST |
| `netlify.toml` | `products.json` bla cache bach l changements ybanou direct |
| `README.md` | Had l fichier |

## Questions fréquentes

- **L Admin kaygoul "login" o ma kaydkholch ?** → Identity wla Git Gateway mazal ma t-activawch (step 3), wla l invitation ma t-acceptatch.
- **Bdellit produit walakin l site ma tbeddelch ?** → Tsennna 1 minute (Netlify kay-redeployi), o refreshe l page b `Ctrl + F5`.
- **Bghit nbeddel l numéro WhatsApp ?** → Kayn f `index.html` : `WHATSAPP_NUMBER = "212600457896"`.
- **L site l9dim (drag-and-drop) mazal khdam ?** → Iyeh, `tubular-ganache-e4b159.netlify.app` khdam, walakin bla Admin. Melli tconnecti GitHub, l site jdid howa li ghadi ykhdem.
