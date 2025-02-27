# Changelog
All notable changes to this project will be documented in this file. This project adheres to [Semantic Versioning](http://semver.org/).

## 2.4.1

* Fix: validation of Redis context parameters array in server hook no longer fails (#315) (#317)
* Enhance: move some settings related code out of main class (#321)
* Maintenance: Tested up to WordPress 6.7


## 2.4.0

Requires PHP 5.6 and WordPress 4.7 or above

* New: introduce Redis (also KeyDB and Valkey) support using the _phpredis_ module (#253), (#252, props @newtovaux)
* New: add `cachify_modify_output` filter
* New: add `cachify_create_gzip_files` to disable creation of static GZip files (#262, props @angcl)
* New: add hooks `cachify_removed_cache_by_url` and `cachify_flushed_total_cache` for additional actions after clearing (#294, props @ouun)
* Removed: APC support (#304)
* Enhance: adjust styling for setup instructions (#215, props @timse201)
* Enhance: update hooks for Multisite initialization in WordPress 5.1 and above (#246, props @ouun)
* Enhance: rework flush hooks and add some third-party triggers for Autoptimize and WooCommerce (#225, props @timse201)
* Enhance: clean up some internal error suppressions (#256)
* Enhance: inform user on cache clear in admin bar (#257, props @angcl)
* Enhance: do not flush the cache for post revisions (#261, props @angcl)
* Enhance: prevent unnecessary cache clearing in some cases (#223) (#224, props @timse201)
* Enhance: remove empty directories when clearing the HDD cache (#289)
* Enhance: introduce common interface for caching backends (#298, props @lloc)
* Enhance: enhance examples for .htaccess and nginx configuration (#302)
* Enhance: show admin notice instead of silent fallback to DB cache, if selected backend is unavailable (#305)
* Enhance: disable gzip creation of required PHP extension is missing (#308)
* Enhance: various internal code clean ups
* Fix: invalidate cache when permalink changes (#285, #286, props @raffaelj)
* Fix: remove empty directories when pruning the HDD cache (#289)
* Fix: correctly add user-agent to robots.txt (#282) (#283)
* Fix: exclude _sitemap.xml_ from caching (#242) (#254)
* Fix: prevent cache generation of non-GET requests (#200) (#258)
* Fix: prevent cache generation of requests with status different from 200 OK (#266) (#267, props @karlkowald)
* Fix: prevent cache generation of non-HTML responses when using content negotiation (#265) (#273, props @Ancocodet)
* Fix: fix styling for various dark mode plugins (#264) (#278)
* Fix: fix SVG markup for icons in dashboard widget (#269, props @Latz)
* Fix: added missing .gz suffix in htaccess (#287) (#291, props @raffaelj)
* Fix: fix some brand names and unify spelling (#297, props @pedro-mendonca)
* Maintenance: Tested up to WordPress 6.6


## 2.3.2
* Fix: enforce WordPress environment for caching modules (#221, props timse201)
* Fix: Remove unnecessary build artifacts from plugin deployment (#226)
* Fix: Fix input sanitization for APC proxy (#240) (#241)
* Maintenance: Remove unused language folder (#214, props timse201)
* Maintenance: Update documentation links (#211, #212, props timse201)
* Maintenance: Update documentation links (#213, props timse201)
* Maintenance: More precise tags in README file (#216, props timse201)
* Maintenance: Tested up to WordPress 5.8

## 2.3.1
* Fix: clean up unused parameter evaluation after publishing a post to prevent PHP notice (#187) (#188)
* Fix: correct minor spelling mistakes (#193, props timse201)
* Fix: update support links (#194, props timse201)

## 2.3.0
* New: WP-CLI integration (#165, props derweili)
* New: `cachify_flush_cache_hooks` filter added to modify all hooks that flush the cache
* New: Flush cache when a user is created / updated / deleted
* New: Flush cache when a term is created / updated / deleted (#169, props derweili)
* New: Cache behavior after post modification is now configurable in plugin settings (#176)
* Enhance: Cache exceptions/User-Agents translation (#52, props timse201)
* Enhance: Readme FAQ (#51, props timse201)
* Enhance: sizeable exclusion boxes + placeholder (#53, props timse201)
* Enhance: FAQ and Support links (#55, props timse201)
* Enhance: Add text caption to "flush cache" button
* Enhance: Icon font converted to SVG (#64)
* Enhance: Improved HDD cache invalidation for hierarchical post types (#71, props Syberspace)
* Enhance: Unified and shortened HTML signature across all caching methods (#108) (#109)
* Security: Tabnabbing prevention (#55, props timse201)
* Maintenance: Tested up to WordPress 5.4


## 2.2.4
* Fixes caching for mixed HTTPS and HTTP setups
* Fixes an issue with the icon styling in the admin toolbar
* Ensures compatibility with the latest WordPress version

## 2.2.3
* New: Generated a POT file
* New: Added German formal translation
* Updated, translated + formatted README.md
* Updated expired link URLs in plugin and languages files
* Updated plugin authors

## 2.2.2
* Fix: parameter return by filter dashboard_glance_items
* Generous use of the filter esc_html

## 2.2.1
* Fix for the PHP notice "Call to undefined function is_plugin_active_for_network" on WordPress Multisite

## 2.2.0
* Toolbar: Display of the "Flush the Cachify cache" button on the frontend
* Toolbar: Controlling the display of the "Flush the Cachify cache" button via hook

## 2.1.9
* Vervollständigung des Cachify-Pfades in `robots.txt`: `Disallow: /wp-content/cache/cachify/`
* *Release-Zeitaufwand (Development & QA): 0,75 Stunden*

## 2.1.8
* HHVM-Unterstützung für die *Memcached* Caching-Methode (Danke, [Ulrich Block](http://www.ulrich-block.de))

## 2.1.7
* Cache-Leerung bei Custom Post Types
* Einführung zusätzlicher Sicherheitsabfragen
* Code-Refactoring

## 2.1.6
* Button "Cache leeren" sichtbar sowohl in WP 3.8 wie WP 3.9

## 2.1.5
* Support für WordPress 3.9
* Button "Cache leeren" sichtbar bei jeder Bildschirmauflösung

## 2.1.4
* Support für WordPress 3.8.1

## 2.1.3
* Manuelle Auswahl: Beim Artikel-Update nur den Seitencache löschen
* Lokalisierung der Plugin-Dateien
* Umbauten am Plugin-Core
* Detaillierter auf [Google+](https://plus.google.com/+SergejMüller/posts/By2PEtRMk8g)

## 2.1.2
* Optimierung für WordPress 3.8
* Option hinzugefügt: Neue Kommentare lösen einen Cache-Reset aus

## 2.1.1
* Hook `cachify_skip_cache` für die Steuerung der Cache-Generierung
* Support für das MP6 Plugin
* Detaillierter auf [Google+](https://plus.google.com/110569673423509816572/posts/S1mpFsG3NZC)

## 2.1.0
* Cache-Leerung bei Plugin-Deaktivierung

## 2.0.9
* Quelltext-Minimierung als Selektbox und Hook
* Interne Umstellung auf Konstanten

## 2.0.7
* Unterstützung für Memcached
* WordPress 3.6 Support
* Cache-Neuaufbau beim Theme-Wechsel
* Quelltext-Optimierungen

## 2.0.6
* Cache-Neuaufbau einer Blogseite nur bei Kommentaren, die freigegeben sind

## 2.0.5
* Cache-Leerung nach einem WordPress-Upgrade
* Keine Cache-Ausgabe für Jetpack Mobile Theme
* Abfrage auf eingeloggte Nutzer bei APC als Caching-Methode
* Änderung der Systemvoraussetzungen
* Cache-Reset nach WordPress-Update

## 2.0.4
* Bessere Trennung der Cache-Gesamtgröße im Dashboard-Widget "Auf einen Blick"

## 2.0.3
* Cache-Leerung beim Veröffentlichen verfügbarer Custom Post Types
* Noindex in der von WordPress generierten `robots.txt` für den Ordner mit HDD-Cache
* Hook `cachify_flush_cache` zum Leeren des Cache aus Drittanwendungen

## 2.0.2
* Unterstützung für WordPress 3.4
* Hochauflösende Icons für iPad & Co.
* Anpassungen für ältere PHP5-Versionen
* Entfernung des Plugin-Icons aus der Sidebar

## 2.0.1
* Verbesserter Autoload-Prozess
* Diverse Umbenennungen der Optionen
* Cache-Neuaufbau bei geplanten Beiträgen (Cachify DB)

## 2.0
* Überarbeitung der GUI
* Source Code-Modularisierung
* Cache-Größe auf dem Dashboard
* Festplatte als Ablageort für Cache
* Produktseite online: http://cachify.de
* Cache-Neuaufbau bei Kommentarstatusänderungen
* APC-Anforderungen: APC 3.0.0, empfohlen 3.1.4
* Optional: Kein Cache für kommentierende Nutzer
* Schnellübersicht der Optionen als Inline-Hilfe
* Mindestanforderungen: WordPress 3.1 & PHP 5.1.2

## 1.5.1
* `zlib.output_compression = Off` für Apache Webserver

## 1.5
* Überarbeitung des Regexp für HTML-Minify
* Reduzierung des Toolbar-Buttons auf das Icon
* Formatierung und Kommentierung des Quelltextes

## 1.4
* Xmas Edition

## 1.3
* Unterstützung für APC (Alternative PHP Cache)
* Umpositionierung des Admin Bar Buttons

## 1.2.1
* Icon für die "Cache leeren" Schaltfläche in der Admin Bar

## 1.2
* Schaltfläche "Cache leeren" in der Adminbar (ab WordPress 3.1)
* `flush_cache` auf public gesetzt, um von [wpSEO](http://wpseo.de "WordPress SEO Plugin") ansprechen zu können
* Ausführliche Tests unter WordPress 3.3

## 1.1
* Interne Prüfung auf fehlerhafte Cache-Generierung
* Anpassungen an der Code-Struktur
* Entfernung der Inline-Hilfe
* Verknüpfung der Online-Hilfe mit Optionen

## 1.0
* Leerung des Cache beim Aktualisieren von statischen Seiten
* Seite mit Plugin-Einstellungen
* Inline-Dokumentation in der Optionsseite
* Ausschluss von Passwort-geschützten Seiten
* WordPress 3.2 Support
* Unterstützung der WordPress Multisite Blogs
* Umstellung auf den template_redirect-Hook (Plugin-Kompatibilität)
* Interne Code-Bereinigung

## 0.9.2
* HTML-Kompression
* Flattr-Link

## 0.9.1
* Cache-Reset bei geplanten Beiträgen
* Unterstützung für das Carrington-Mobile Theme

## 0.9
* Workaround für Redirects

## 0.8
* Blacklist für PostIDs
* Blacklist für UserAgents
* Ausnahme für WP Touch
* Ausgabe des Zeitpunktes der Generierung
* Umbenennung der Konstanten

## 0.7
* Ausgabe des Speicherverbrauchs

## 0.6
* Live auf wordpress.org
