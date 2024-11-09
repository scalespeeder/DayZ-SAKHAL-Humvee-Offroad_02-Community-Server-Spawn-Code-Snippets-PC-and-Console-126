1.26 Sakhal Code Snippets To Bring Humvee Events ( Offroad_02 ) To The Winter Map Files README

Instructionss & code snippets to bring Humvee events to Sakhal, on PC & PlayStation & Xbox Console Community Servers..

A maximum of 3 humvees will spawn at a possible 22 locations. (See supplied image for locations).

Humvees will spawn in complete with cans of fuel in the inventory, but damage will be variable.

Individual Humvee parts, wheels & the glow plug are not set to spawn in the economy, they're only on the vehicles.

The glow-plug can be used to run the military bunker generator...

Limited Testing on PC SAKHAL Local PC Server & Xbox Community Server Version 1.26 NOV 2024.

Edited by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

------

INSTRUCTIONS

Stop your server & make back-ups of the files we're about to edit, events.xml & cfgeventspawns.xml.

It's best to download files & edit locally on your PC if you can.

Check all edits with an online XML validator: https://www.xmlvalidation.com/

Navigate to & open the events.xml file on your sever ( DayZServer\mpmissions\dayzOffline.sakhal\db )

Search for the "VehicleOffroadHatchback" event, and after the closing   </event> tag, paste the following extra entry: 

 <event name="VehicleOffroad02"><!-- this is the humvee-->
        <nominal>3</nominal>
        <min>2</min>
        <max>3</max>
        <lifetime>300</lifetime>
        <restock>0</restock>
        <saferadius>500</saferadius>
        <distanceradius>500</distanceradius>
        <cleanupradius>200</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>fixed</position>
        <limit>mixed</limit>
        <active>1</active>
        <children>
            <child lootmax="0" lootmin="0" max="3" min="2" type="Offroad_02"/>
        </children>
    </event>
	

Save your file & validate to check for errors. Upload if OK.

Navigate to & open the cfgeventspawns.xml file on your sever ( DayZServer\mpmissions\dayzOffline.sakhal )

At the bottom of the file, above </eventposdef> paste the following XML code snippet:

	<event name="VehicleOffroad02">
		<pos x="5719.51" y="4.7592" z="4349.69" a="-2.60123"/>
		<pos x="5321.28" y="3.45799" z="4850.36" a="-9.99419"/>
		<pos x="5052.24" y="31.4471" z="3821.01" a="-0.392962"/>
		<pos x="4660.85" y="6.08474" z="5211.66" a="5.25554"/>
		<pos x="3878.43" y="7.83121" z="5497.16" a="-33.3859"/>
		<pos x="2909.95" y="10.1216" z="5665.61" a="-0.0234691"/>
		<pos x="2923.01" y="39.3063" z="6325.57" a="131.275"/>
		<pos x="2914.57" y="41.0084" z="6828.88" a="-160.563"/>
		<pos x="2168.6" y="32.0343" z="7429.23" a="-133.41"/>
		<pos x="1120.31" y="8.49235" z="7611.56" a="1.21276"/>
		<pos x="1396.5" y="65.0339" z="7911.31" a="16.8113"/>
		<pos x="2364.19" y="4.18634" z="8573.83" a="-6.103"/>
		<pos x="2657.23" y="8.63476" z="9250.05" a="-20.2515"/>
		<pos x="3618.79" y="29.197" z="9522.54" a="-163.207"/>
		<pos x="3715.72" y="10.6164" z="9321.42" a="60.5927"/>
		<pos x="3961.92" y="4.66933" z="9063.93" a="-0.539329"/>
		<pos x="4291.6" y="6.20429" z="8933.01" a="0.433005"/>
		<pos x="7107.31" y="3.68399" z="7115.82" a="-17.2414"/>
		<pos x="7230.17" y="3.71256" z="7588.65" a="-13.1797"/>
		<pos x="10314.8" y="248.842" z="8539.17" a="19.7379"/>
		<pos x="12072.7" y="180.498" z="9702.05" a="166.174"/>
		<pos x="8198.72" y="219.72" z="11984" a="-44.1114"/>
	</event>
		
 Save your file & validate to check for errors. Upload if OK.
 
Navigate to & open the cfgspawnabletypes.xml file on your server ( DayZServer\mpmissions\dayzOffline.sakhal )

and find the <type name="Offroad_02"> entry. Replace it with the following code (paste it over the top):

<type name="Offroad_02">
		<attachments chance="1.00">
			<item name="Offroad_02_Wheel" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Wheel" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Wheel" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Wheel" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Wheel" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Trunk" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Hood" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Door_1_1" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Door_1_2" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Door_2_1" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="Offroad_02_Door_2_2" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="HeadlightH7" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="GlowPlug" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CarBattery" chance="1.00" />			  
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="CanisterGasoline" chance="1.00" />
		</attachments>
		<attachments chance="1.00">
			<item name="TacticalBaconCan" chance="0.25" />
		</attachments>
		<attachments chance="1.00">
			<item name="SodaCan_Spite" chance="0.25" />
		</attachments>
	</type> 
 
 Save your file & validate to check for errors. Upload if OK.
 
 Restart your server & enjoy!
 
Thanks, Rob.



