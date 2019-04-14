# Fixing the Issue with WR for Deathrun & Briefing

Your Minecraft client likely will not connect to the _speedrun.com/API & Lergin_ servers to retrieve the data.

Minecraft comes with a own Java version, just in case you don't have one installed. This is `1.8.0 Version 23`.
The problem is, Minecraft is not trusting the aforementioned servers. Only Java programs with a higher version than `1.8.0 Version 101` trust the _speedrun.com / Lergin_ servers.

***

Important for this is that you have such a Java version installed on your computer.
One option is to run `java -version` in a command prompt.
Or you can check on the _Apps & Features_ page in Windows.
If you have a sufficient Java version try to find its JRE executable in your Explorer.
If not, update Java.
By default, these are located at `C:\Program Files\Java\jre1.8.0_VERSION\bin\javaw.exe`
or `C:\Program Files (x86)\Java\jre1.8.0_VERSION\bin\javaw.exe`

If nothing helps, you can also ask me at _ItsNiklass#3108_ or _@ItsNiklass_

**Note: If you're using the old launcher or a custom one like MultiMC, you don't need to proceed any further. Just make sure your Java is up-to-date.**

***

To tell Minecraft to go and use your updated Java version, we have to go into the launcher:
_(Images below)_


**1 - Go into your Launch options.**

**2 - Select your active profile you are using Beezig with.**

**3 - Turn on the custom Java executable.**

**4 - Select your own javaw.exe in your new Java directory and click Save**

**5 - WR should now work. Contact me if issues still exists :)**

***

![](https://i.imgur.com/iJt60YT.png)

![](https://i.imgur.com/7I2g6x2.png)

![](https://i.imgur.com/HSWEPsm.png)
