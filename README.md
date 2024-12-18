# Список вразливостей веб-сервера cPanel

Публікується з метою контролю безпеки сайтів на базі веб-серверів з cPanel. На замітку дослідникам та власникам електронних ресурсів. В рамках волонтерського проєкту "За вільний і безпечний UAnet!".

Дані вразливості були виявлені дослідниками KR. Laboratories в ході глобального аудиту ресурсів українського сегменту мережі Інтернет й можуть бути використані як легітимними пентестерами, так і зловмисниками для проведення таких атак як: переповнення буфера (buffer overflow), Denial of Service / Distributed Denial of Service Attack (DoS/DDoS), Path Traversal, Local File Inclusion / Remote File Inclusion (LFI/RFI), Cross Site Scripting Attack (XSS), Cross Site Request Forgery / Server Side Request Forgery (CSRF/SSRF), розкриття конфіденційної інформації (Expose Sensitive Information / Information Disclosure), пошкодження або втрата даних, помилки конфігураці та багато інших.   

Ми рекомендуємо українським веб-майстрам і системним адміністраторам регулярно оновлювати серверне програмне забезпечення та використовувати наші рекомендації щодо кібербезпеки, аби мінімізувати потенційні ризики.  

З приводу захисту веб-серверів пишіть нам на електронну скриньку: security[@]kr-labs.com.ua

| **CVE Ідентифікатор** &nbsp; &nbsp; &nbsp; &nbsp; | **Опис** | **Exploit / PoC** |
|-----------------------------------------------------|----------|-------------|
| [**CVE-2003-1425**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2003-1425)| guestbook.cgi в cPanel 5.0 дозволяє віддаленим зловмисникам виконувати довільні команди за допомогою параметра шаблону. | [Експлойт](https://www.exploit-db.com/exploits/22263) |
| [**CVE-2004-1769**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2004-1769)| Функція «Дозволити користувачам cPanel скидати свій пароль електронною поштою» в cPanel дозволяє віддаленим зловмисникам виконувати довільний код за допомогою параметра користувача для resetpass. | [Деталі](https://blog.sucuri.net/2019/10/an-indirect-way-to-change-cpanel-passwords.html) |
| [**CVE-2008-7142**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-7142)| Вразливість абсолютного проходження шляху в модулі використання диска (frontend/x/diskusage/index.html) у cPanel дозволяє віддаленим зловмисникам створювати список довільних каталогів за допомогою параметра showtree. | [Експлойт](https://www.exploit-db.com/exploits/31439) |
| [**CVE-2008-1499**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-1499)| Вразливість міжсайтового сценарію (XSS) у frontend/x/manpage.html. | [Експлойт](https://www.exploit-db.com/exploits/31472) |
| [**CVE-2008-2070**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-2070)| Інтерфейс WHM для cPanel дозволяє віддаленим зловмисникам обходити захист від XSS й впроваджувати довільний сценарій або HTML за допомогою повторюваних, неправильно впорядкованих символів "<" та ">". | [Експлойт](https://www.exploit-db.com/exploits/31773) [Деталі](https://seclists.org/fulldisclosure/2008/May/269) |
| [**CVE-2008-2478**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-2478)| Scripts/wwwacct у cPanel дозволяє віддаленим автентифікованим користувачам із повноваженнями виконувати довільний код за допомогою метасимволів оболонки в полі електронної адреси. | [Експлойт](https://www.exploit-db.com/exploits/31807) |
| [**CVE-2021-31589**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-31589)| cPanel не обмежує належним чином перезапис файлів | [PoC](https://github.com/karthi-the-hacker/CVE-2021-31589) |
| [**CVE-2022-47532**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-47532)| FileRun 20220519 дозволяє впровадження SQL через параметр "dir" у запиті /?module=users&section=cpanel&page=list. | N/A |
| [**CVE-2022-48623**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-48623)| Пакет Cpanel::JSON::XS для Perl здійснює доступ поза межами поля (out-of-bounds) таким чином, що зловмисники можуть отримати конфіденційну інформацію або спричинити відмову в обслуговуванні (DoS). | N/A |
| [**CVE-2023-29489**](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-29489)| XSS-вразливість виникає на сторінці помилки cpsrvd (cpanelwebcall) через недійсний ідентифікатор веб-виклику, він же SEC-669. | [PoC1](https://github.com/xKore123/cPanel-CVE-2023-29489) [PoC2](https://github.com/md-thalal/CVE-2023-29489) [PoC3](https://github.com/mdaseem03/cpanel_xss_2023) [Експлойт](https://sploitus.com/exploit?id=A9B2E12E-7C0B-5943-9D14-7C26EE00669F) [Деталі](https://www.assetnote.io/resources/research/finding-xss-in-a-million-websites-cpanel-cve-2023-29489) [Video](https://www.youtube.com/watch?v=Q6DZTs8xLTc) |

### Джерела
- [CVE Mitre cPanel](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=cPanel)
- [cPanel/WHM Change log](https://docs.cpanel.net/changelogs/)
- [cPanel Security Bounty Program](https://cpanel.net/cpanel-security-bounty-program/)
- [Exploit-DB cPanel](https://www.exploit-db.com/?search=cpanel)
- [cPanel Roadmap](https://features.cpanel.net/tabs/11-planned-roadmap)
- [Cpanel WHM Exploit](https://github.com/UND3F3IND/cpanel-whm-ssh-ftp-exploit)
- [Sucuri Blog. An Indirect Way to Change cPanel Passwords](https://blog.sucuri.net/2019/10/an-indirect-way-to-change-cpanel-passwords.html)
- [cPanel ports](https://blog.sucuri.net/2023/11/https-protocol-what-is-the-default-port-for-ssl-common-tcp-ports.html)
- [Bobcares. How to fix HTTPoxy vulnerability in cPanel, Plesk or other Linux / Windows servers](https://bobcares.com/blog/fix-httpoxy-vulnerability-cpanel-plesk-linux-windows/)
- [imunify360. cPanel hacks: How to protect your cPanel account](https://blog.imunify360.com/cpanel-hacks-how-to-protect-your-cpanel-account)
- [Sucuri Blog. Bash Vulnerability – Shell Shock – Thousands of cPanel Sites are High Risk](https://blog.sucuri.net/2014/09/bash-vulnerability-shell-shock-thousands-of-cpanel-sites-are-high-risk.html)
- [gbhackers. cPanel 2FA Bypass Exposes Tens of Millions of Websites to Hack](https://gbhackers.com/cpanel-2fa-bypass/)
