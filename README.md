# emsâl ⚖︎

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/) ![GitHub followers](https://img.shields.io/github/followers/dgknrsln?style=social)

<sup>[TR]</sup> Yargıtay karar arama [arayüzünden](https://karararama.yargitay.gov.tr/YargitayBilgiBankasiIstemciWeb/) kararların, yıl ve karar numarası temelinde yarı otomatik olarak indirilmesini sağlayan Python kütüphanesi.

<sup>[EN]</sup> A Python library that enables semi-automatic downloading of decisions based on year and decision number from the Supreme Court decision search [interface](https://karararama.yargitay.gov.tr/YargitayBilgiBankasiIstemciWeb/).

## ➥Yükleme / Installation

```emsâl```, pip paket yönetim sistemi kullanarak yüklenebilir.

You can use pip package manager system to install ```emsâl```.
```bash 
  pip install emsal
```
  
## ➥Kullanım / Usage

    import emsal

    emsal.get_decisions(driver_path, '2019', last_no='1978')

## ➥Nasıl çalışır? / How does it work?

<sup>[TR]</sup> ```emsâl``` kütüphanesi temel olarak girdi olarak verilen yılda, belirtilen karar numarası aralığındaki, ilgili anahtar kelimeyi geçiren kararları (en fazla bin adet olmak üzere) bulunulan dizine metin belgesi olarak kaydeder.

Programı çalıştırdığınızda aşağıdaki gif'te görüleceği üzere program otomatik olarak anahtar kelime, tarih ve karar numarası kutularını doldurur ve ardından Captcha'yı girmeniz için 10 saniye bekler. Ardından kararları tek tek ilgili dizine kaydeder. Bu noktadan sonra bir şey yapmanıza gerek yoktur. Sistem kararları biner biner getirdiği için, 1000 karar sonra program otomatik olarak durur. Eğer devam etmek istiyorsanız kaldığınız karar numarasından tekrar başlamanız gerekir.

<sup>[EN]</sup> The ```emsâl``` library basically saves the decisions (maximum one thousand) that include the relevant keyword in the specified decision number range and in the given year as a text document in the current directory.

When you run the program, the program automatically fills in the keyword, date and decision number boxes, as can be seen in the gif below, and then waits 10 seconds for you to enter the Captcha. Then it saves the decisions one by one in the relevant directory. You don't need to do anything after this point. The program stops automatically after 1000 decisions, as the system fetches the decisions one thousand at a time. If you want to continue, you have to start again from the decision number where you left off.