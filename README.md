# Readme

This is the August export of the scans database of Pittsburgh Parking Authority's Automatic License Plate Reader program. Every entry represents a single license plate scan.

For background, see this <a href="http://www.post-gazette.com/neighborhoods-city/2013/09/22/Pittsburgh-s-parking-authority-snaps-200K-motorists-a-month/stories/201309220010">Post-Gazette article on the program</a>. The American Civil Liberties Union has a <a href="https://www.aclu.org/alpr">good report on ALPR programs nationwide</a>.

The database structure:

<table>
	<thead>
		<tr>
			<th>Field</th>
			<th>Type</th>
			<th>Purpose</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>ID</td>
			<td>int</td>
			<td>Unique identifier</td>
		</tr>
		<tr>
			<td>DateTime</td>
			<td>timestamp with date</td>
			<td>Timestamp of when scan was made.</td>
		</tr>
		<tr>
			<td>Plate</td>
			<td>text</td>
			<td>License plate number of scanned car.</td>
		</tr>
		<tr>
			<td>State</td>
			<td>text</td>
			<td>State that issued scanned license plate; frequently "?"</td>
		</tr>
		<tr>
			<td>SideReadFrom</td>
			<td>text</td>
			<td>Which camera picked up the vehicle; RIGHT usually means the scanned vehicle was parked, while LEFT indicates a car passing in the opposing lane.</td>
		</tr>
		<tr>
			<td>Lat</td>
			<td>float</td>
			<td>Latitude of scan point.</td>
		</tr>
		<tr>
			<td>Lng</td>
			<td>float</td>
			<td>Longitude of scanned point</td>
		</tr>
		<tr>
			<td>AlarmFlag</td>
			<td>text</td>
			<td>"TRANSIT" if scanned car had no fines; "ALARM" if it did.</td>
		</tr>
		<tr>
			<td>Fine</td>
			<td>float</td>
			<td>Accumulated fine on scanned vehicle; reads "Not available" if no fine.</td>
		</tr>
		<tr>
			<td>CarID</td>
			<td>int</td>
			<td>Numeric ID of the camera car that recorded the license plate.</td>
		</tr>
		  
		
	</tbody>

</table>
