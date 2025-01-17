<details><!-- components dropdown -->
<summary>components</summary>

<!-- name_parts dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>name_parts</summary>
  <p>Three lists full of parts of names. AI generated</p>
  <details style="margin-left: 2em; font-family: sans-serif;">
    <summary>name_start_parts</summary>
    <p>
      Type: list<br>
      A list containing small strings, supposed to contain typical starting parts of a name.
    </p>
  </details>
  <details style="margin-left: 2em; font-family: sans-serif;">
    <summary>name_middle_parts</summary>
    <p>
      Type: list<br>
      A list containing small strings, supposed to contain typical middle parts of a name.
    </p>
  </details>
  <details style="margin-left: 2em; font-family: sans-serif;">
    <summary>name_end_parts</summary>
    <p>
      Type: list<br>
      A list containing small strings, supposed to contain typical ending parts of a name.
    </p>
  </details>
</details> <!-- end of name_parts dropdown -->

<!-- race dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>race</summary>
<pre><code class="language-python">race(name: str, strength_modifier: int, constitution_modifier: int, intelligence_modifier: int, agility_modifier: int)
</code></pre>
</details> <!-- end of race dropdown -->

<!-- profession dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>profession</summary>
<pre><code class="language-python">profession(name: str)
</code></pre>
</details> <!-- end of profession dropdown -->

<!-- character dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>character</summary>
<!-- start of character setup code -->
<pre><code class="language-python">character(race:race,profession:profession,name:str,initiative = 0,strength = 10,constitution = 10,intelligence = 10,agility = 10,armor_class = 4,max_health=10)</code></pre> 
Example
  <pre><code class="language-python">commoner = profession("commoner")
human = race("Human", 0, 0, 0, 0)
player = character(human,commoner,genname())</code></pre>
<!-- end of character setup code -->

<!-- start of create_random dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>create_random()</summary> 
  Randomizes character stats
  <pre><code class="language-python">create_random(self)</code></pre>
  Example
  <pre><code class="language-python">commoner = profession("commoner")
human = race("Human", 0, 0, 0, 0)
player = character(human,commoner,genname())
player.create_random()</code></pre>
</details><!-- end of create_random dropdown -->

<!-- start of printstats dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>printstats()</summary> 
  Displays character stats
  <pre><code class="language-python">printstats(self)
</code></pre>
  Example
  <pre><code class="language-python">commoner = profession("commoner")
human = race("Human", 0, 0, 0, 0)
player = character(human,commoner,genname())
player.create_random()
player.printstats()</code></pre>
</details><!-- end of printstats dropdown -->

<!-- start of printinvent dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>printinvent()</summary> 
  Displays character inventory
  <pre><code class="language-python">printinvent(self)
</code></pre>
  Example
  <pre><code class="language-python">commoner = profession("commoner")
human = race("Human", 0, 0, 0, 0)
player = character(human,commoner,genname())
player.create_random()
player.printinvent()</code></pre>
</details><!-- end of printinvent dropdown -->

<!-- start of equip_weapon dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>equip_weapon(weapon:weapon,from_invent = False)</summary> 
  Equips a weapon to a character weapon slot
  <pre><code class="language-python">equip_weapon(self,weapon:weapon,from_invent = False)
</code></pre>
  <p><b>-</b> If from_invent is True, a TypeError will return shall the specefied weapon not exist in the character inventory</p>
  Example
  <pre><code class="language-python">commoner = profession("commoner")
sword = weapon("sword", 2, "a sword", (2,6), 0)
human = race("Human", 0, 0, 0, 0)
player = character(human,commoner,genname())
player.create_random()
player.equip_weapon(sword)</code></pre>
</details><!-- end of equip_weapon dropdown -->

<!-- start of attack dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
  <summary>attack(target:character)</summary>
  Attacks a target
  <pre><code class="language-python">attack(self,target:character)
</code></pre>
  <p><b>-</b> Roll to hit, on hit, deal damamge to target based on equiped weapon and attack roll</p>
  Example
  <pre><code class="language-python">commoner = profession("commoner")

sword = weapon("sword", 2, "a sword", (2,6), 0)
human = race("Human", 0, 0, 0, 0)  

enemy = character(human,commoner,genname())
enemy.create_random()

player = character(human,commoner,genname())
player.create_random()
player.equip_weapon(sword)
player.attack(enemy)
</code></pre>
</details><!-- end of attack dropdown -->

<!-- start of aquire dropdown -->
<details style="margin-left: 2em; font-family: sans-serif;">
<summary>aquire(target:any)</summary>
Places an item in the character inventory
  <pre><code class="language-python">aquire(self,target:any)</code></pre>
  <p><b>-</b> The target must have the is_pickable attribute set to True or else a TypeError is raised</p>
  Example
  <pre><code class="language-python">commoner = profession("commoner")
bread = food("Bread",0.2,"It's bread",2)
human = race("Human",0,0,0,0
player = character(human,commoner,genname())
player.create_random()
player.aquire(bread)</code></pre>
</details><!-- end of equip_weapon dropdown -->
</details> <!-- end of character dropdown -->
</details><!-- end of components dropdown -->

<details>
  <summary>basics</summary>
  
  ### Item 1
  Some content for item 1.
  
  ### Item 2
  Some content for item 2.
  
  ### Item 3
  Some content for item 3.

</details>
<details>
  <summary>generators</summary>
  
  ### Item 1
  Some content for item 1.
  
  ### Item 2
  Some content for item 2.
  
  ### Item 3
  Some content for item 3.

</details>
<details>
  <summary>items</summary>
  
  ### Item 1
  Some content for item 1.
  
  ### Item 2
  Some content for item 2.
  
  ### Item 3
  Some content for item 3.

</details>
<details>
  <summary>errors</summary>
  
  ### Item 1
  Some content for item 1.
  
  ### Item 2
  Some content for item 2.
  
  ### Item 3
  Some content for item 3.

</details>