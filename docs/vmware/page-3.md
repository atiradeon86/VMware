#Virutalizáció, VMware alapok

A virtualizáció legfőbb célja a rendelkezésre álló erőforrások kihasználásának maximalizálása, főleg a mai világban, amikor ugrásszerűen emelkednek az elérhető CPU magok, és azok teljesítménye.

**Legfőbb előnyei:**

- egyszerű migráció / flexibilis környezet
- erőforrások maximális kihasználása
- erőforrások egyszerű átcsoportosítása, módosítása (pl. CPU, RAM, Storage)
- terhelés elosztás
- biztonságos izoláció
- snapshot kezelés
- clusterek kialakítása

Nagyon szuper lehetőség különböző rendszerek tanulásához, teszteléséhez, hogy egyszerre egy időben akár több különböző operációs rendszert is tudunk futtatni, és mindezt elfogadható sebességgel.

Ezektől függetlenül a fő potenciál a szerverek esetében érhető tetten. Hatalmas előrelépés ez, hiszen nem szükséges minden adott dedikált feladatra külön fizikai gép beállítása.

Egy adott szerver funkciót el tudunk különíteni akár külön virtuális gépekre is, aminél külön erőforrás managementet is csinálhatunk.


**Type 1** virtualizácó (Bare Metal)

A hypervisor közvetlenül a hardveren fut, a virtuális gép erőforrásainak biztosításával.

**Type2** virtualizáció (Hosted)

A hypervisor a host operációs rendszeren fut.

**Nested virtualizáció**

A beágyazott virtualizálás egy olyan funkció, amely lehetővé teszi pl. egy ESXi host virtuális gépen való futtatását. Más szóval a beágyazott virtualizálással maga az ESXi is virtualizálható.

**Hypervisor**

A hypervisor olyan szoftver, ami virtuális számítógépek futtatását végzi.

**ESXi**

Maga a hypervisor. Futhat Type1, és Type2 rendszerként is Nested virtualizációban. Ingyenesen használható, regisztráció után licensz igényelhető hozzá a VMware oldalán.

**vSphere**

Minden komolyabb funkcióhoz szükség van rá, tulajdonképpen egy Appliance, amit egy már létező ESXi host-ra lehet deploy-olni. Fizetős, 60 napos próbaverzió elérhető, a lehetőségek kipróbálásához beállítások gyakorlásához teljesen jó.

**SAN**

A Storage Area Network, azaz a tárolóhálózat, tároló alrendszerekből és hozzájuk tartozó hálózati infrastruktúrából áll.

A tároló eszközök általában valamilyen gyors hálózati kapcsolaton keresztül, jellemzően legalább 10 Gbit-es kapcsolaton csatlakoznak egymáshoz, és az azokat közös megosztott tárhelyként használó eszközökhöz.

Megfelelő sebességű infrastruktúra esetén ez rengeteg előnnyel jár, amit pl. a vMotion, vagy DRS segítségével ki is tudunk használni.

Itt is hatalmas előny, hogy az adattárolókat teljes méretükben ki tudjuk használni, nincs veszteség a tárolókapacitásból.


