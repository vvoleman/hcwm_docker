# HCWM
## Instalace
1. Naklonujte tento repozitář
2. Tento repozitář slouží jako nadřazený repozitář pro všechny ostatní repozitáře, které jsou součástí projektu. Všechny ostatní repozitáře jsou podřízené repozitáři `hcwm` a jsou v něm jako podmoduly. Proto je nutné při naklonování repozitáře použít klíč `--recursive`, aby se získaly i podmoduly.
   ```sh
       git clone --recursive git@github.com:vvoleman/hcwm_docker.git
   ```
3. Spusťte příkaz `docker-compose up --build` pro spuštění projektu.
4. Je nutné ještě provést pár příkazů ručně
   1. docker exec -it hcwm_web_back bash
      1. composer install
      2. php bin/console doctrine:migrations:migrate
      3. php bin/console doctrine:fixtures:load
      4. php bin/console app:zotero:load

## Odkazy na ostatní repozitáře
- [HCWM Backend](https://github.com/vvoleman/hcwm)
- [HCWM Frontend](https://github.com/vvoleman/hcwm_front)
- [HCWM Translator](https://github.com/vvoleman/hcwm_translator)
  - V současné chvíli neexistuje, ale zkoušel jsem použít několik offline řešení.
  