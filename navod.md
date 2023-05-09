# Předpoklady

- Fyzický počítač nebo VPS s operačním systémem Windows, GNU/Linux, MacOS, FreeBSD, OpenBSD nebo Androidem
- Nejlépe alespoň 4GB RAM a procesor s dobrým jednojádrovým výkonem
- Rychlé připojení k internetu v obou směrech (nejlépe alespoň 50MB/s)
- Přístup k nastavení routeru (není nutné u VPS)

# Návod

## 1. Vyberte si server

Pro Minecraft existuje velké množství různých serverů, drtivá většina z nich založených na oficiálním Minecraftovém serveru napsaném v Javě. Většina těch, které na oficiálním serveru založené nejsou jsou nekompletní nebo zastaralé, většinou používané ve velmi technicky náročných scénářích, se kterými se pravděpodobně nesetkáte, proto se o nich v tomto tutoriálu nebudu zmiňovat.

Než ale začneme, musíte se rozhodnout zdali chcete aby se mohli připojit hráči s oficiálním, neupraveným klientem Minecraftu, nebo zdali chcete hrát s modifikacemi, které nejde implementovat čistě na serveru. Instalací modifikací ztratíte část potenciálních hráčů, kteří si použité modifikace nebudou ochotní nainstalovat, ale umožní vám si server více do hloubky přizpůsobit. Pro hraní s modifikacemi, které jsou nekompatibilní s oficiálním Minecraftem jsou vhodné následující servery:

- [Forge](https://files.minecraftforge.net/net/minecraftforge/forge/) - Načítač modifikací s dlouhou historií a velkou knihovnou modifikací, ale typicky pomalejším výkonem než oficiální server, zvláště u velkých modpacků, často se používá se staršími verzemi Minecraftu
- [Fabric](https://fabricmc.net/) - Načítač modifikací nekompatibilní s Forge, napsaný tak, aby byl výkonnější než Forge a se správnými modifikacemi mnohem rychlejší než i oficiální server, má menší knihovnu modifikací, většina z nich pro nejnovější verzi Minecraftu
- [Quilt](https://quiltmc.org/en/) - Načítač modifikací založený na Fabric, aktuálně kompatibilní s ním, zatím se příliš nedoporučuje používat, jelikož je v ranné fázi vývoje

Dále existují servery, pro které není potřeba speciální klient

- [Oficiální server Minecraftu](https://www.minecraft.net/en-us/download/server) - Nedoporučuje se používat kvůli špatnému výkonu, telemetrii, špatné rozšiřitelnosti a funkcím reportování hráčů
- Bukkit - Jeden z prvních neoficiálních serverů (už neaktualizovaný), zakládá se na něm Spigot, Paper, Purpur a další, které jsou s ním kompatibilní, nedoporučuje se používat kvůli jeho zastaralosti a omezenosti, na rozdíl od "modů" je rozšiřován "pluginy"
- [Spigot](https://www.spigotmc.org/) - Založený na Bukkitu, rozšiřuje jej o dodatečné API, podporuje většinu dostupných pluginů
- [Paper](https://papermc.io/) - Modifikace Spigotu s cílem většího výkonu a bezpečnosti, přidává další API, může být problematický pokud jde o perfektní kompatibilitu s oficiálním Minecraftem (opravuje některé chyby na kterých závisí některé redstonové stroje)
- [Purpur](https://purpurmc.org/) - Další rozšíření Paperu o další API s ještě agresivnějšími optimalizacemi
- [Fabric](https://fabricmc.net/) a [Quilt](https://quiltmc.org/en/) - Pokud použijete pouze serverové modifikace, kterých je pro Fabric a Quilt velké množství, můžete dosáhnout velkých výkonů na serveru, který je velmi kompatibilní s oficiálním serverem, lze také jednoduše zamaskovat jako oficiální server
- [Sponge](https://spongepowered.org/) - Alternativní server s API pro pluginy, které je modernější, ale nekompatibilní s žádným jiným načítačem pluginů, proto má menší knihovnu

Ve chvíli co jste si vybrali server, který chcete je potřeba stáhnout si jeho serverový .jar soubor. Tyto soubory lze typicky stáhnout z jejich oficiálních stránek, až na Spigot, který kvůli obavám z autorských práv vyžaduje aby si každý uživatel [sám sestavil Spigot](#).

## Nainstalujte Javu

Jelikož je Minecraft program založený na Javě, je potřeba nainstalovat Javu na počítač, který bude server spouštět. Toto není tak jednoduché, jak by se mohlo zdát, jelikož existuje mnoho variant Javy. Dvě hlavní jsou ty vyráběné od Oracle:

- [Java SE](https://www.java.com/en/) - původní, nesvobodná, ale bezplatná verze Javy, tuto verzi má nainstalovanou většina uživatelů Windows, má delší dobu podpory než OpenJDK
- [OpenJDK](https://openjdk.org/) - výkonově a funkčně téměř identická verze Javy pod svobodnou licencí, rovněž bezplatná, tuto verzi používá oficiální Minecraftový spouštěč

Dále nabízí mnoho firem upravené verze OpenJDK s podporou srovnatelnou nebo delší než Java SE. Pro tento návod je jedno, kterou variantu využijete, ale ideálně nainstalujte pro servery pro novější verzi Minecraftu verzi 17, jelikož pro tuto verzi je Minecraft navržen a je dlouhodobě podporovaná. V tomto návodu si ukážeme jak nainstalovat OpenJDK. Tato instalace je ale jiná pro každý operační systém.

### GNU/Linux

Většina distribucí Linuxu nabízí OpenJDK ve svých oficiálních repozitářích. Je proto vhodné nainstalovat OpenJDK ze svého oficiálního repozitáře. Níže jsou příkazy pro různé 

- Debian, Ubuntu: `sudo apt install openjdk-17-jdk`
- Arch Linux: `tohle napíše honza`
- Fedora: `sudo dnf install java-17-openjdk-devel.x86_64`
