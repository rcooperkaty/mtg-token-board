<h1>Commander Token Board</h1>

<p><strong>Commander Token Board</strong> is a lightweight, mobile-optimized web application designed to replace physical tokens, dice, and dry-erase boards during <em>Magic: The Gathering</em> Commander games.</p>

<p>It operates as a single-file HTML application (<code>index.html</code>), meaning it requires no installation, no server, and no internet connection (unless fetching card art). It is designed to feel like a native app when added to your mobile home screen.</p>

<hr>

<h2>🚀 Key Features</h2>

<ul>
    <li><strong>Mobile-First Design:</strong> Optimized for touchscreens with large hit areas, swipe-friendly layouts, and OLED-black themes to conserve battery during long games.</li>
    <li><strong>Wake Lock:</strong> Automatically prevents your device from going to sleep while the board is visible.</li>
    <li><strong>Smart Image Layering:</strong> The app prioritizes image sources in this order: <em>User Upload &gt; Scryfall Art (if enabled) &gt; Local File &gt; Text Fallback</em>. You will never see a "broken image" icon.</li>
    <li><strong>Deck Parsing:</strong> Import a text-based decklist to automatically generate a roster of required tokens.</li>
</ul>

<hr>

<h2>🕹️ Interaction Guide</h2>

<p>The interface relies on gesture-based controls to keep the screen uncluttered.</p>

<h3>1. Controlling Tokens</h3>
<p>Once a token is on the battlefield, you interact with it using specific taps:</p>

<ul>
    <li><strong>Single Tap:</strong> Taps (rotates) or Untaps the creature.
        <ul>
            <li><em>Note:</em> If a creature has <strong>Summoning Sickness</strong> (ZZZ icon), a single tap will "shake" the card to remind you it cannot attack yet.</li>
        </ul>
    </li>
    <li><strong>Double Tap:</strong> Opens the <strong>Context Menu</strong>.
        <ul>
            <li><em>Why Double Tap?</em> This prevents accidental deletions or edits during gameplay.</li>
            <li><strong>Context Menu Options:</strong>
                <ul>
                    <li><strong>Tap X:</strong> Tap a specific number of tokens in a stack (e.g., "Attack with 5 of my 10 Goblins").</li>
                    <li><strong>Add Keyword:</strong> Add badges like <em>Flying</em>, <em>Trample</em>, or <em>Deathtouch</em>.</li>
                    <li><strong>Edit / Transform:</strong> Modify the stats, color, or name (useful for Clones or Transform mechanics).</li>
                    <li><strong>Destroy:</strong> Remove a single token or the entire stack.</li>
                </ul>
            </li>
        </ul>
    </li>
    <li><strong>Buttons:</strong>
        <ul>
            <li><strong>+1/+1 &amp; -1/-1:</strong> Instantly adjust power/toughness counters.</li>
            <li><strong>Clone:</strong> Creates a copy of the token (resetting summoning sickness).</li>
        </ul>
    </li>
</ul>

<h3>2. The "Next Turn" Cycle</h3>
<p>A floating button labeled <strong>"Next Turn ↺"</strong> appears when you have tokens on the board. Clicking this performs the cleanup step:</p>
<ol>
    <li><strong>Untaps</strong> all tapped tokens.</li>
    <li><strong>Removes Summoning Sickness</strong> from all creatures.</li>
    <li><strong>Consolidates Stacks:</strong> If you have multiple stacks of identical tokens (e.g., two piles of "3/3 Beast"), it merges them into a single stack to save screen space.</li>
</ol>

<hr>

<h2>🛠️ Adding Tokens</h2>

<h3>Quick Add (Presets)</h3>
<p>The sidebar allows you to search for common tokens.</p>
<ul>
    <li><strong>Tap:</strong> Adds 1 copy of the token to the board (with Summoning Sickness).</li>
    <li><strong>Long Press:</strong> Opens a configuration menu <em>before</em> adding, allowing you to change the quantity or stats immediately.</li>
</ul>

<h3>Custom Tokens</h3>
<p>For specific board states (e.g., "A Copy of my Opponent's Sol Ring"), use the <strong>Custom Token</strong> panel:</p>
<ul>
    <li><strong>Name &amp; Stats:</strong> Manually enter Power/Toughness and Color.</li>
    <li><strong>Search Real Card:</strong> Check this box to fetch the official art from Scryfall API.</li>
    <li><strong>Upload Image:</strong> Upload a custom image (like a "Waifu Rabbit" or a photo of your pet). This image is saved to the browser's temporary session memory.</li>
</ul>

<h3>Deck Import</h3>
<ol>
    <li>Open the <strong>Menu (☰)</strong> and select <strong>+ Add Deck</strong>.</li>
    <li>Paste your decklist (from Moxfield, Archidekt, TappedOut, etc.).</li>
    <li>The app scans the list against the Scryfall database.</li>
    <li>It identifies every card that <em>produces</em> a token and adds those specific tokens to your "Quick Add" list automatically.</li>
</ol>

<hr>

<h2>📋 Default Preset Library</h2>

<p>The application comes pre-loaded with <strong>28</strong> of the most common token types found in the Commander format.</p>

<table border="1" cellpadding="8" cellspacing="0" width="100%">
  <thead>
    <tr bgcolor="#333333">
      <th><font color="white">Token Name</font></th>
      <th><font color="white">Color</font></th>
      <th><font color="white">Stats (P/T)</font></th>
      <th><font color="white">Notes</font></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Angel</b></td>
      <td>White</td>
      <td>4/4</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Beast</b></td>
      <td>Green</td>
      <td>3/3</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Bird</b></td>
      <td>Blue</td>
      <td>1/1</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Cat</b></td>
      <td>White</td>
      <td>2/2</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Clue</b></td>
      <td>Colorless</td>
      <td>0/0</td>
      <td>Artifact - Clue</td>
    </tr>
    <tr>
      <td><b>Construct</b></td>
      <td>Colorless</td>
      <td>0/0</td>
      <td>Variable Stats</td>
    </tr>
    <tr>
      <td><b>Demon</b></td>
      <td>Black</td>
      <td>5/5</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Dragon</b></td>
      <td>Red</td>
      <td>4/4</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Drake</b></td>
      <td>Blue</td>
      <td>2/2</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Elf Warrior</b></td>
      <td>Green</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Food</b></td>
      <td>Colorless</td>
      <td>0/0</td>
      <td>Artifact - Food</td>
    </tr>
    <tr>
      <td><b>Goblin</b></td>
      <td>Red</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Golem</b></td>
      <td>Colorless</td>
      <td>3/3</td>
      <td>Artifact</td>
    </tr>
    <tr>
      <td><b>Human</b></td>
      <td>White</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Insect</b></td>
      <td>Green</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Knight</b></td>
      <td>White</td>
      <td>2/2</td>
      <td>Vigilance (often)</td>
    </tr>
    <tr>
      <td><b>Myr</b></td>
      <td>Colorless</td>
      <td>1/1</td>
      <td>Artifact</td>
    </tr>
    <tr>
      <td><b>Pegasus</b></td>
      <td>White</td>
      <td>1/1</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Plant</b></td>
      <td>Green</td>
      <td>0/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr bgcolor="#f0f0f0">
      <td><b>Rabbit</b></td>
      <td><b>White</b></td>
      <td><b>1/1</b></td>
      <td><b>New Addition</b></td>
    </tr>
    <tr>
      <td><b>Rat</b></td>
      <td>Black</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Saproling</b></td>
      <td>Green</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Soldier</b></td>
      <td>White</td>
      <td>1/1</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Spirit</b></td>
      <td>White</td>
      <td>1/1</td>
      <td>Flying</td>
    </tr>
    <tr>
      <td><b>Thopter</b></td>
      <td>Colorless</td>
      <td>1/1</td>
      <td>Artifact - Flying</td>
    </tr>
    <tr>
      <td><b>Treasure</b></td>
      <td>Colorless</td>
      <td>0/0</td>
      <td>Artifact - Treasure</td>
    </tr>
    <tr>
      <td><b>Wolf</b></td>
      <td>Green</td>
      <td>2/2</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td><b>Zombie</b></td>
      <td>Black</td>
      <td>2/2</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>💾 Data Persistence</h2>
<ul>
    <li><strong>Board State:</strong> Your current board (tokens, counts, tap states) is saved to your browser's <code>localStorage</code>. If you refresh the page or close the browser, your board will be exactly how you left it.</li>
    <li><strong>Images:</strong> Custom uploaded images are stored in the active session. <strong>Note:</strong> If you clear your browser cache, custom images may be lost, but the token stats will remain.</li>
</ul>
