# Cmder/ConEmu Color Schemes

Color schemes for [Cmder](https://cmder.app/) & [ConEmu](https://conemu.github.io/) terminal emulators

## Example

<br/>

- Flow

![FLow color scheme](screenshot/Flow_sce.png?raw=true)  
<br/>

- Flow light

![Flow light color scheme](screenshot/Flow_light_sce.png?raw=true)

## Setting

<br/>

**`Add a color scheme via ConEmu config. file`**
<br/>
<br/>

1.  Open **`ConEmu.xml`** file. It is in the:

    - `Cmder\vendor\conemu-maximus5\` <sup>_(Cmder)_</sup>
    - ConEmu installation directory <sup>_(ConEmu)_</sup>
    - user directory like `C:\Users\UserName`  
      <br/>

2.  Look for a `Colors` key in the `ConEmu.xml` config. file

    - Paste the color scheme as suggested by the comment  
      <br/>

        ```xml
        <?xml version="1.0" encoding="utf-8"?>
        <key name="Software">
            <key name="ConEmu">
    	        <key name=".Vanilla" modified="2022-09-26 18:57:18" build="210912">
    	            <!-- Other ConEmu configuration -->
    	            <key name="Colors" modified="2022-09-23 18:21:05" build="210912">
    		        <value name="Count" type="long" data="01"/>
    		        <!-- Paste color-scheme.xml content here -->
    		        <!-- Other palettes -->
    	            </key>
    	        </key>
            </key>
        </key>
        ```

    _`ConEmu.xml` **might not contain** `Colors` key._ _In that case do next:_  
    <br/>

3.  Generate `Colors` key

    - Open _Settings > Features > Colors_
    - Create a new custom color scheme and specify a name
    - Press `Save` button

    This will generate a `Colors` key in the `ConEmu.xml` config. file.  
    <br/>

4.  Update the pallette number `<key name="Palette(X)"` if required.  
    e.g. if there is 1 custom color palette already, it should be `Palette2` for the new one.

    ```xml
    <key name="Palette2" modified="2022-09-23 15:37:34" build="210912">
    ```

    <br/>

5.  Increment the value of `Count` key after the `Colors` key. The `Count` should be the total number of palettes configured under `Colors` key.

    ```xml
    <value name="Count" type="long" data="02"/>
    ```

    The following example shows `Colors` key, the modified part of `ConEmu.xml` config. file.

    ```xml
    <key name="Colors" modified="2022-09-23 18:21:05" build="210912">
        <value name="Count" type="long" data="02"/>
        <key name="Palette1" modified="2022-09-15 16:20:35" build="210912">
            <value name="Name" type="string" data="some-color-scheme"/>
            <!-- Palette values -->
            <value name="ColorTable15" type="dword" data="00939fa0"/>
        </key>
        <key name="Palette2" modified="2022-09-23 15:37:34" build="210912">
            <value name="Name" type="string" data="Flow"/>
            <value name="TextColorIdx" type="hex" data="10"/>
            <value name="BackColorIdx" type="hex" data="10"/>
            <value name="PopTextColorIdx" type="hex" data="10"/>
            <value name="PopBackColorIdx" type="hex" data="10"/>
            <value name="ColorTable00" type="dword" data="00383226"/>
            <value name="ColorTable01" type="dword" data="00ac7f2a"/>
            <value name="ColorTable02" type="dword" data="00699a78"/>
            <value name="ColorTable03" type="dword" data="00716f5d"/>
            <value name="ColorTable04" type="dword" data="004a3dcb"/>
            <value name="ColorTable05" type="dword" data="005a4fbc"/>
            <value name="ColorTable06" type="dword" data="00b8b0a1"/>
            <value name="ColorTable07" type="dword" data="00ebebeb"/>
            <value name="ColorTable08" type="dword" data="006a5f57"/>
            <value name="ColorTable09" type="dword" data="00ffc440"/>
            <value name="ColorTable10" type="dword" data="003ed7a5"/>
            <value name="ColorTable11" type="dword" data="00c1ac00"/>
            <value name="ColorTable12" type="dword" data="005252ff"/>
            <value name="ColorTable13" type="dword" data="008140ff"/>
            <value name="ColorTable14" type="dword" data="0046bcee"/>
            <value name="ColorTable15" type="dword" data="00aeaaa6"/>
        </key>
    </key>
    ```

    <br/>
	
6.  Reopen Cmder or ConEmu
