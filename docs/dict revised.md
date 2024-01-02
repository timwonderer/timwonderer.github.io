---


---

<h3 id="span-classbluedictionary-unordered-mutable-unique-key-value-referenced"><span class="blue">Dictionary: <em>Unordered, Mutable, Unique Key-Value referenced</em></span></h3>
<h4 id="span-classbg-yellowi-classfa-fa-file-i-creating-a-dictionary"><span class="bg-yellow"><i class="fa fa-file "></i> Creating a Dictionary</span></h4>
<p>A <strong>dictionary</strong> is a collection type that maps a unique key to a value. Elements in a dictionary are assigned a unique key, which can be any immutable object such as string, integer, floating-point number, or tuple.</p>
<p>To create a dictionary, use a colon <code>:</code> to create key-value pairings, and separate each pairing with a comma <code>,</code>. Enclose all elements in curly braces <code>{}</code>.</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment"># Create a dictionary with names of animals as keys</span>
myFriends <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">"Leon"</span><span class="token punctuation">:</span> <span class="token string">"lion"</span><span class="token punctuation">,</span> <span class="token string">"Tuxy"</span><span class="token punctuation">:</span> <span class="token string">"penguin"</span><span class="token punctuation">,</span> <span class="token string">"Benjie"</span><span class="token punctuation">:</span> <span class="token string">"hippo"</span><span class="token punctuation">}</span>

<span class="token comment"># Displaying the elements in the dictionary</span>
<span class="token keyword">print</span><span class="token punctuation">(</span>myFriends<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-python3"><code class="prism .run:height=&quot;250px&quot; language-python3"># Create a dictionary with names of animals as keys
myFriends = {"Leon": "lion", "Tuxy": "penguin", "Benjie": "hippo"}

# Displaying the elements in the dictionary
print(myFriends)
</code></pre>
<h4 id="span-classbg-yellowi-classfa-fa-file-i-keyvalue-reference-in-a-dictionary"><span class="bg-yellow"><i class="fa fa-file "></i> Key:Value Reference in a Dictionary</span></h4>
<p>Each key-value pairing is like a remote key fob for a car. Each car has a <strong>unique key fob code</strong> that <strong>unlocks a specific car</strong>. <em>Each key fob is assigned to one car</em>.</p>
<p><img src="https://www.scaler.com/topics/images/dict-in-python_thumbnail.webp" alt="enter image description here"></p>
<p>When retrieving an element from a dictionary, provide the key that’s mapped to the element. <strong>Each key in the dictionary must be unique.</strong></p>
<p>For example, we have mapped the <em>key</em> <code>"name"</code> to the <em>value</em> of <code>"Ron"</code> in the dictionary image above. If we try to store the <em>value</em> <code>"Harry"</code> to the <em>key</em> <code>"name"</code>, the dictionary will replace the old value <code>"Ron"</code> with the new value <code>"Harry"</code>.</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment"># Create the dictionary</span>
employee <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">'name'</span><span class="token punctuation">:</span> <span class="token string">'Ron'</span><span class="token punctuation">,</span> <span class="token string">'age'</span><span class="token punctuation">:</span> <span class="token string">'25'</span><span class="token punctuation">,</span> <span class="token string">'job'</span><span class="token punctuation">:</span> <span class="token string">'Dev'</span><span class="token punctuation">}</span>

<span class="token comment"># Display the elements in the dictionary</span>
<span class="token keyword">print</span><span class="token punctuation">(</span>employee<span class="token punctuation">)</span>

<span class="token comment"># Assign a new value to the key 'name'</span>
employee<span class="token punctuation">[</span><span class="token string">'name'</span><span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token string">'Harry'</span>

<span class="token comment"># Display the updated dictionary</span>
<span class="token keyword">print</span><span class="token punctuation">(</span>employee<span class="token punctuation">)</span>
</code></pre>
<pre class=" language-python3"><code class="prism .run:height=&quot;250px&quot; language-python3"># Create the dictionary
employee = {'name':'Ron', 'age':'25', 'job':'Dev'}

# Display the elements in the dictionary
print (employee)

# Assign new value to the key 'name'
employee['name'] = 'Harry'

# Display the elements in the dictionary afterwards
print (employee)
</code></pre>
<h4 id="span-classbg-yellowi-classfa-fa-file-i-dictionary-is-unordered-sort-of"><span class="bg-yellow"><i class="fa fa-file "></i> Dictionary is Unordered (sort of)</span></h4>
<p>Lists are <strong>sequenced</strong> and <strong>referenced using indices</strong> representing the <strong>position</strong> of the element in the list.</p>
<p><strong>Dictionaries do not use indices</strong> for element referencing, as their entries are <strong>unordered</strong>. This means you cannot reference the elements in a dictionary using an index because <em>it doesn’t exist</em>.</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment"># Create a dictionary with names of animals as keys</span>
myFriends <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">"Leon"</span><span class="token punctuation">:</span> <span class="token string">"lion"</span><span class="token punctuation">,</span> <span class="token string">"Tuxy"</span><span class="token punctuation">:</span> <span class="token string">"penguin"</span><span class="token punctuation">,</span> <span class="token string">"Benjie"</span><span class="token punctuation">:</span> <span class="token string">"hippo"</span><span class="token punctuation">}</span>

<span class="token comment"># Attempting to get an index will raise an AttributeError</span>
<span class="token comment"># print(myFriends.index("Leon"))</span>
</code></pre>
<pre class=" language-python3"><code class="prism .run:height=&quot;300px&quot; language-python3"># Create a dictionary with names of animals as keys
myFriends = {"Leon": "lion", "Tuxy": "penguin", "Benjie": "hippo"}

# Attempting to get an index will raise an AttributeError
print(myFriends.index("Leon"))
</code></pre>
<p>The reason for this is because dictionary data structure is <em>fundamentally different from a list</em>.</p>
<p>A <strong>list</strong> has index because <strong>elements are stored sequentially and those sequence is preserved</strong>.  You can also <strong>sort</strong> the elements in a list because lists have actual sequence where there is a <em>first element and a last element</em>.</p>
<p>A <strong>dictionary</strong> pairs a key to a value using what is known as a <em>hashtable</em>. When a dictionary is created, the program creates a table that <strong>records the key and the exact memory address of the value</strong>. This allows the dictionary to locate the value very quickly compared to a list, which needs to go down the list to arrive at the specific index. As a result, dictionary elements cannot be sorted because their is not such thing as “<em>first position</em>” or “<em>last position</em>” in a dictionary</p>
<p>While a dictionary is efficient in looking up values, it does take up <strong>more memory spaces</strong> because it need extra space to create the mapping.</p>
<hr>
<h3 id="span-classbluecoffee-shop-rewards-program-revisitedspan"><span class="blue">Coffee Shop Rewards Program Revisited</span></h3>
<p>Because <strong>dictionary has a unique key:value pair structure</strong>, we can take advantage of this for our coffee shop rewards program problem introduced at the beginning of this entire series.</p>

<table>
<thead>
<tr>
<th>Customer</th>
<th>Points</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kim</td>
<td>23</td>
</tr>
<tr>
<td>Knives</td>
<td>55</td>
</tr>
<tr>
<td>Wallace</td>
<td>45</td>
</tr>
<tr>
<td>Steven</td>
<td>12</td>
</tr>
<tr>
<td>Scott</td>
<td>77</td>
</tr>
<tr>
<td>Young Neil</td>
<td>132</td>
</tr>
<tr>
<td>Ramona</td>
<td>5</td>
</tr>
<tr>
<td>Matthew</td>
<td>87</td>
</tr>
<tr>
<td>Lucas</td>
<td>44</td>
</tr>
<tr>
<td>Gideon</td>
<td>14</td>
</tr>
</tbody>
</table><p>For our coffee shop rewards program, we can store the <span class="red"><strong>customer’s name</strong></span> as the <span class="red"><strong>key</strong></span> and their <span class="green"><strong>reward points</strong></span> as the <span class="green"><strong>value</strong>.</span></p>
<pre class=" language-python"><code class="prism  language-python">customerRewards <span class="token operator">=</span> <span class="token punctuation">{</span>
    <span class="token string">'kim'</span><span class="token punctuation">:</span> <span class="token number">23</span><span class="token punctuation">,</span> <span class="token string">'knives'</span><span class="token punctuation">:</span> <span class="token number">55</span><span class="token punctuation">,</span> <span class="token string">'wallace'</span><span class="token punctuation">:</span> <span class="token number">45</span><span class="token punctuation">,</span> <span class="token string">'steven'</span><span class="token punctuation">:</span> <span class="token number">12</span><span class="token punctuation">,</span>
    <span class="token string">'scott'</span><span class="token punctuation">:</span> <span class="token number">77</span><span class="token punctuation">,</span> <span class="token string">'youngNeil'</span><span class="token punctuation">:</span> <span class="token number">132</span><span class="token punctuation">,</span> <span class="token string">'ramona'</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token string">'matthew'</span><span class="token punctuation">:</span> <span class="token number">87</span><span class="token punctuation">,</span>
    <span class="token string">'lucas'</span><span class="token punctuation">:</span> <span class="token number">44</span><span class="token punctuation">,</span> <span class="token string">'gideon'</span><span class="token punctuation">:</span> <span class="token number">14</span>
<span class="token punctuation">}</span>
</code></pre>
<p>To retrieve a specific customer’s reward points, we can use</p>
<pre class=" language-python"><code class="prism  language-python">dictionaryName<span class="token punctuation">[</span>key<span class="token punctuation">]</span>
</code></pre>
<p>Which takes in the key as argument and returns the value corresponding to the key. We can also update the reward points value by using</p>
<pre class=" language-python"><code class="prism  language-python">dictionaryName<span class="token punctuation">[</span>key<span class="token punctuation">]</span> <span class="token operator">=</span> newValue
</code></pre>
<p>Which takes in the key as an argument and updates the value corresponding to the key with <code>newValue</code></p>
<p>Now let’s see how this works in action!</p>
<pre class=" language-python"><code class="prism  language-python"><span class="token comment"># Dictionary storing customer name and points</span>
customerRewards <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">'kim'</span><span class="token punctuation">:</span><span class="token number">23</span><span class="token punctuation">,</span> <span class="token string">'knives'</span><span class="token punctuation">:</span><span class="token number">55</span><span class="token punctuation">,</span>
                   <span class="token string">'wallace'</span><span class="token punctuation">:</span><span class="token number">45</span><span class="token punctuation">,</span> <span class="token string">'steven'</span><span class="token punctuation">:</span><span class="token number">12</span><span class="token punctuation">,</span>
                   <span class="token string">'scott'</span><span class="token punctuation">:</span><span class="token number">77</span><span class="token punctuation">,</span> <span class="token string">'youngNeil'</span><span class="token punctuation">:</span><span class="token number">132</span><span class="token punctuation">,</span>
                   <span class="token string">'ramona'</span><span class="token punctuation">:</span><span class="token number">5</span><span class="token punctuation">,</span> <span class="token string">'matthew'</span><span class="token punctuation">:</span><span class="token number">87</span><span class="token punctuation">,</span>
                   <span class="token string">'lucas'</span><span class="token punctuation">:</span><span class="token number">44</span><span class="token punctuation">,</span> <span class="token string">'gideon'</span><span class="token punctuation">:</span><span class="token number">14</span><span class="token punctuation">}</span>

<span class="token comment"># Prompt user input customer name                 </span>
customerName <span class="token operator">=</span> <span class="token builtin">input</span> <span class="token punctuation">(</span><span class="token string">"Enter the customer's name: "</span><span class="token punctuation">)</span>

<span class="token comment"># Pretend the user type in "scott"</span>
customerName <span class="token operator">=</span> <span class="token string">'scott'</span>

<span class="token comment"># Display point values</span>
<span class="token keyword">print</span> <span class="token punctuation">(</span>customerName<span class="token punctuation">,</span> <span class="token string">"has reward points of"</span><span class="token punctuation">,</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token punctuation">,</span><span class="token string">"points."</span><span class="token punctuation">)</span>

<span class="token comment"># Prompt user input for operation</span>
operation <span class="token operator">=</span> <span class="token builtin">input</span> <span class="token punctuation">(</span><span class="token string">"For redeem, press 1. For add points, press 2:"</span><span class="token punctuation">)</span>

<span class="token comment"># Pretend the user choose to add points</span>
operation <span class="token operator">=</span> <span class="token number">2</span>

<span class="token comment"># Conditional code for operation</span>
<span class="token keyword">if</span> operation <span class="token operator">==</span> <span class="token number">1</span><span class="token punctuation">:</span>
    redemption <span class="token operator">=</span> <span class="token builtin">input</span> <span class="token punctuation">(</span><span class="token string">"Please enter the number of drinks redeemed: "</span><span class="token punctuation">)</span>
    <span class="token keyword">if</span> redemption<span class="token operator">*</span><span class="token number">25</span> <span class="token operator">&lt;=</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token punctuation">:</span>
        customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span> <span class="token operator">=</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token operator">-</span><span class="token punctuation">(</span>redemption<span class="token operator">*</span><span class="token number">25</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span><span class="token punctuation">:</span>
        <span class="token keyword">print</span><span class="token punctuation">(</span><span class="token string">"Not enough points"</span><span class="token punctuation">)</span>
        <span class="token keyword">pass</span>
<span class="token keyword">elif</span> operation <span class="token operator">==</span> <span class="token number">2</span><span class="token punctuation">:</span>
    update <span class="token operator">=</span> <span class="token builtin">int</span><span class="token punctuation">(</span><span class="token builtin">input</span> <span class="token punctuation">(</span><span class="token string">"Please enter the purchase amount rounded up to nearest dollars:"</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
    update <span class="token operator">=</span> <span class="token number">15</span>
    <span class="token keyword">if</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token operator">+</span>update <span class="token operator">&lt;=</span> <span class="token number">250</span><span class="token punctuation">:</span>
        customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span> <span class="token operator">=</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span> <span class="token operator">+</span> update
        <span class="token keyword">print</span> <span class="token punctuation">(</span><span class="token string">"The updated point value for"</span><span class="token punctuation">,</span> customerName<span class="token punctuation">,</span> <span class="token string">"is:"</span><span class="token punctuation">,</span>customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token punctuation">)</span>
    <span class="token keyword">else</span><span class="token punctuation">:</span>
        customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token number">250</span>
        <span class="token keyword">print</span> <span class="token punctuation">(</span><span class="token string">"Max point value reached. The updated poitn value is"</span><span class="token punctuation">,</span> customerRewards<span class="token punctuation">[</span>customerName<span class="token punctuation">]</span><span class="token punctuation">)</span>


</code></pre>
<pre class=" language-python3"><code class="prism .run language-python3"># Dictionary storing customer name and points
customerRewards = {'kim':23, 'knives':55,
                   'wallace':45, 'steven':12,
                   'scott':77, 'youngNeil':132,
                   'ramona':5, 'matthew':87,
                   'lucas':44, 'gideon':14}

# Prompt user input customer name                 
customerName = input ("Enter the customer's name: ")

# Pretend the user type in "scott"
customerName = 'scott'

# Display point values
print (customerName, "has reward points of", customerRewards[customerName],"points.")

# Prompt user input for operation
operation = input ("For redeem, press 1. For add points, press 2:")

# Pretend the user choose to add points
operation = 2

# Conditional code for operation
if operation == 1:
    redemption = input ("Please enter the number of drinks redeemed: ")
    if redemption*25 &lt;= customerRewards[customerName]:
        customerRewards[customerName] = customerRewards[customerName]-(redemption*25)
    else:
        print("Not enough points")
        pass
elif operation == 2:
    update = int(input ("Please enter the purchase amount rounded up to nearest dollars:"))
    update = 15
    if customerRewards[customerName]+update &lt;= 250:
        customerRewards[customerName] = customerRewards[customerName] + update
        print ("The updated point value for", customerName, "is:",customerRewards[customerName])
    else:
        customerRewards[customerName] = 250
        print ("Max point value reached. The updated poitn value is", customerRewards[customerName])


</code></pre>
<hr>
<h3 id="span-classbluedictionary-operations-and-methodsspan"><span class="blue">Dictionary operations and methods</span></h3>
<p>Just like list, Python has many built-in operations and methods (functions specific to a particular type) for dictionary. <a href="https://books.trinket.io/pfe/09-dictionaries.html"><strong>You should read the chapter on dictionary here</strong></a> and pratice using them to manage data.</p>
<p><strong>Here are some dictionary methods</strong></p>
<blockquote>
<p>In the table below, <em>dict</em> represents the name of the dictionary. For example: <code>dict.get("scott")</code> will return the value for the key <code>"scott"</code> from the dictionary named <code>dict</code></p>
</blockquote>

<table>
<thead>
<tr>
<th><strong>Methods</strong></th>
<th><strong>What does it do?</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>dict.clear()</td>
<td>removes all items from the dictionary</td>
</tr>
<tr>
<td>dict.copy()</td>
<td>returns a copy of the dictionary without modifying the original</td>
</tr>
<tr>
<td>dict.fromkeys(<em>keys</em>, <em>values</em>)</td>
<td>create a dictionary using elements from an iterable (list, string, set, etc.) as keys and values of any type or elements from another iterable as values.</td>
</tr>
<tr>
<td>dict.get(<em>key</em>)</td>
<td>returns the value assigned to the specified key</td>
</tr>
<tr>
<td>dict.items()</td>
<td>returns a view object that displays a list of a given dictionary’s key:value pair as tuples</td>
</tr>
<tr>
<td>dict.keys()</td>
<td>extracts the keys of the dictionary and returns the list of keys as view objects</td>
</tr>
<tr>
<td>dict.popitem()</td>
<td>removes and return the latest key:value pair in the dictionary</td>
</tr>
<tr>
<td>dict.setdefault(<em>key</em>, <em>defaultValue</em>)</td>
<td>search the dictionary for the specified key and create a key:defaultValue pair if the key is not in the dictionary</td>
</tr>
<tr>
<td>dict.pop(<em>key</em>)</td>
<td>removes and return an element with the specified key</td>
</tr>
<tr>
<td>dict.values()</td>
<td>returns a view object that displays a list of all values in the dictionary</td>
</tr>
<tr>
<td>dict.update(<em>dictionary</em>)</td>
<td>updates the current dictionary with elements from another dictionary or another iterable key:value pairs (like tuple pairs)</td>
</tr>
</tbody>
</table><hr>
<h3 id="span-classblueconsiderations-for-choosing-dictionary-as-your-data-structurespan"><span class="blue">Considerations for choosing <em>dictionary</em> as your data structure</span></h3>
<p>Just like list, there are some data structure and usage that are better implemented using a dictionary while some are not. Here are some considerations you should have before choosing dictionary to meet your CPT requirements.</p>
<h4 id="span-classgreena-dictionary-might-be-for-you-ifspan"><span class="green">A Dictionary Might Be for You If:</span></h4>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Unique Identifiers Required</strong>: Your data has unique keys that you will use to retrieve values.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Fast Lookups</strong>: You need to quickly access values based on their keys.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Dynamic Data</strong>: You plan to add, remove, or modify key-value pairs.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Heterogeneous Values</strong>: You are storing various types of data, where each key can map to a different data type.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>No Order Dependency</strong>: Your data doesn’t need to be stored or accessed in a specific order.</li>
</ul>
<h4 id="span-classreda-dictionary-might-not-be-suitable-ifspan"><span class="red">A Dictionary Might Not Be Suitable If:</span></h4>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Ordered Data Needed</strong>: You need to maintain a strict order of elements, such as chronological order.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Non-unique Keys</strong>: Your data doesn’t have unique identifiers for each value.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Memory Efficiency</strong>: You are working with a very large amount of data, and memory usage is a concern.</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Simple Data Structure</strong>: Your data structure needs are very simple and don’t require key-value mapping (e.g., a list of numbers).</li>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> <strong>Complex Data Relationship</strong>: Your data has complex relationships that might be better suited to other data structures like graphs or trees.</li>
</ul>
<hr>
<p>###<span class="highlight">Extra Dictionary Functionality</span></p>
<p><strong>As of Python 3.7</strong>, elements in the dictionary <strong>are ordered</strong> based on the <em>insertion order</em>. That order is guaranteed throughout the entire program. However, the order of the dictionary elements is not the same as the index of a list and you cannot reference dictionary elements using their positions.</p>
<p><strong>As of Python 3.7</strong>, elements in dictionary are ordered and can be sorted based on key, value, or other parameters using <code>sorted()</code> function along with <code>items()</code> methods. The syntax would be</p>
<pre class=" language-python"><code class="prism  language-python">sortedDictionary <span class="token operator">=</span> <span class="token builtin">dict</span><span class="token punctuation">(</span><span class="token builtin">sorted</span><span class="token punctuation">(</span>oldDictionary<span class="token punctuation">.</span>items<span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">)</span>
</code></pre>
<p>The <code>items()</code> method returns a list with tuples representing the key:value pairs in the dictionary. The <code>sorted()</code> function allows for custom sorting order (by default, sorting is done based on the first value in the element in ascending order). the <code>dict()</code> constructor converts the sorted list of tuples back into dictionary.</p>

