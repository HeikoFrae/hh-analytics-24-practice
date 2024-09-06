{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## --- FOR LOOP EXERCISES ---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### A List of Fruits"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "apples\n",
      "oranges\n",
      "kiwis\n"
     ]
    }
   ],
   "source": [
    "# Q1: Write a for loop over the keys\n",
    "\n",
    "prices = {'apples': '3.0', 'oranges': '2.5', 'kiwis': '4.0'}\n",
    "\n",
    "for item in prices:\n",
    "    print(item)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "option1\n",
      "\n",
      "apples\n",
      "3.0\n",
      "oranges\n",
      "2.5\n",
      "kiwis\n",
      "4.0\n",
      "\n",
      "option2\n",
      "\n",
      "apples -> 3.0\n",
      "oranges -> 2.5\n",
      "kiwis -> 4.0\n"
     ]
    }
   ],
   "source": [
    "# Q2: Write a for loop to iterate on the keys of the dictionary below and prints both key and the value\n",
    "\n",
    "prices = {'apples': '3.0', 'oranges': '2.5', 'kiwis': '4.0'}\n",
    "\n",
    "print('option1\\n')\n",
    "for key in prices.keys():\n",
    "    print(key)\n",
    "    print(prices[key])\n",
    "\n",
    "print('\\noption2\\n')\n",
    "for key in prices:\n",
    "    print(key, '->', prices[key])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "S\n",
      "P\n",
      "I\n",
      "C\n",
      "E\n",
      "D\n"
     ]
    }
   ],
   "source": [
    "# Q3: For loop needs to iterate over a sequence-like object. Write a for loop to iterate over 'SPICED'\n",
    "\n",
    "for character in 'SPICED':\n",
    "    print(character)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Hi \n",
      "Hi Hi \n",
      "Hi Hi Hi \n",
      "Hi Hi Hi Hi \n"
     ]
    }
   ],
   "source": [
    "# Q4: Write a for loop to  print a triangle(4x4) with 'Hi' (See the pattern below)\n",
    "\n",
    "# Hi \n",
    "# Hi Hi \n",
    "# Hi Hi Hi \n",
    "# Hi Hi Hi Hi\n",
    "\n",
    "\n",
    "# Hint= (start, stop, step)\n",
    "# Hint = default start is 0, default step is 1\n",
    "\n",
    "for i in range(5):\n",
    "    #print(i)\n",
    "    print(i*\"Hi \")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "2\n",
      "4\n",
      "6\n",
      "8\n"
     ]
    }
   ],
   "source": [
    "# Q5\n",
    "for i in range(2,9,2):\n",
    "    print(i)\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Names of Employees"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [],
   "source": [
    "names = ['Alice', 'Bob', 'Charlie', 'Delia']\n",
    "jobs = ['doctor', 'builder', 'cook', 'developer']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Alice works as a doctor\n",
      "Bob works as a builder\n",
      "Charlie works as a cook\n",
      "Delia works as a developer\n"
     ]
    }
   ],
   "source": [
    "# Q5: Write a loop over two lists using zip() which prints 'name works as a job'\n",
    "\n",
    "for name, job in zip(names, jobs):\n",
    "    print(name + ' works as a ' + job)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Q6 write a for loop which prints all the names in the list except 'Charlie'\n",
    "\n",
    "names = ['Alice', 'Bob', 'Charlie', 'Delia']\n",
    "\n",
    "# Hint: if statement and continue\n",
    "\n",
    "# for name in names:\n",
    "#     if name == 'Charlie':\n",
    "#         continue\n",
    "#     print(name)\n",
    "# print(\"The end\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The List with 11 numbers"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Assume that we are working with the list [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]. \n",
    "\n",
    "1. Write a `for` loop to iterate over the list and print each number.\n",
    "2. Add a condition to that for loop which only prints a number if it is even. (**Hint**: use the `%` operator.)\n",
    "\n",
    "    a. Do not only print the even number but store them in the list `evens`.\n",
    "3. Can you modify the condition in question (2) so that the for loop only prints a number if it is odd?\n",
    "4. Now modify the `for` loop so that we print out the index of the elements along with the elements themselves."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[2, 4, 6, 8, 10]\n"
     ]
    }
   ],
   "source": [
    "list8 = [0,1,2,3,4,5,6,7,8,9,10]\n",
    "evens = []\n",
    "for e in list8:\n",
    "    if e % 2 == 0: \n",
    "        evens.append(e)\n",
    "print(evens)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1, 3, 5, 7, 9]\n"
     ]
    }
   ],
   "source": [
    "list8 = [0,1,2,3,4,5,6,7,8,9,10]\n",
    "odds = []\n",
    "for e in list8:\n",
    "    if e % 2 != 0: \n",
    "        odds.append(e)\n",
    "print(odds)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "1 1\n",
      "3 3\n",
      "5 5\n",
      "7 7\n",
      "9 9\n"
     ]
    }
   ],
   "source": [
    "list8 = [0,1,2,3,4,5,6,7,8,9,10]\n",
    "for e in list8:\n",
    "    if e % 2 != 0: \n",
    "        print(list8.index(e), e)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Q8:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [],
   "source": [
    "customer_names = ['KUBIKOM Company GmbH',\n",
    "'Hauser Company',\n",
    "'artofhome Company e.K.',\n",
    "'Atlas Companyservice GmbH',\n",
    "'McRae Company',\n",
    "'Companywerte24.de',\n",
    "'Picaflor Company GmbH',\n",
    "'Behrmann Company GmbH',\n",
    "'Blackert & Borchers Company GmbH & Co KG',\n",
    "'Company Martin Lang',\n",
    "'pleasanthome Company GmbH']\n",
    "\n",
    "customer_names_clean = []\n",
    "\n",
    "for customer in customer_names:\n",
    "    customer_names_clean.append(customer.lower())\n",
    "    "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "['kubikom company gmbh',\n",
       " 'hauser company',\n",
       " 'artofhome company e.k.',\n",
       " 'atlas companyservice gmbh',\n",
       " 'mcrae company',\n",
       " 'companywerte24.de',\n",
       " 'picaflor company gmbh',\n",
       " 'behrmann company gmbh',\n",
       " 'blackert & borchers company gmbh & co kg',\n",
       " 'company martin lang',\n",
       " 'pleasanthome company gmbh']"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "customer_names_clean"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "# this is a very particular solution by a former student. it looks at the examples and uses a special logic that all company short cuts \n",
    "# come after 'company'. in front of 'company' is either nothing or a the actual customer name.\n",
    "\n",
    "customer_names_extracted = []\n",
    "\n",
    "for name in customer_names_clean:\n",
    "    if name.startswith(\"company\"):\n",
    "        s = name.split()\n",
    "        # check if the first element of the variable is only \"company\" or contains \"company\"\n",
    "        if len(s[0]) != len(\"company\"):\n",
    "            customer_names_extracted.append(s[0])\n",
    "        else:\n",
    "            customer_names_extracted.append(' '.join(s[1:]))\n",
    "    elif name.find(\"company\"):\n",
    "        no_com = name.partition(\"company\")\n",
    "        customer_names_extracted.append(no_com[0])\n",
    "\n",
    "print(*customer_names_extracted, sep=\"\\n\")\n",
    "#print(len(customer_names_extracted))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "# this is a more general solution that simply hard codes all the possibilities and checks for them one by one.\n",
    "\n",
    "customer_names_extracted = []\n",
    "\n",
    "for x in customer_names_clean:\n",
    "    if x.endswith('company'):\n",
    "        customer_names_extracted.append(x.replace(' company',''))\n",
    "    elif x.endswith('company gmbh'):\n",
    "        customer_names_extracted.append(x.replace(' company gmbh',''))\n",
    "    elif x.endswith('companyservice gmbh'):\n",
    "        customer_names_extracted.append(x.replace(' companyservice gmbh',''))\n",
    "    elif x.endswith('company e.k.'):\n",
    "        customer_names_extracted.append(x.replace(' company e.k.',''))\n",
    "    elif x.endswith('company gmbh & co kg'):\n",
    "        customer_names_extracted.append(x.replace(' company gmbh & co kg',''))\n",
    "    else:\n",
    "        customer_names_extracted.append(x)\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Q9:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [],
   "source": [
    "email_address_list = [\n",
    "'nolan_mckinney3462@the-quickest.com',\n",
    "'brenk4987@bestmail.us',\n",
    "'hugh_mckay4695@postpro.net',\n",
    "'aline3529@emailplus.org',\n",
    "'vaneldik8972@internetemails.net',\n",
    "'efren1904@imap.cc',\n",
    "'oralia_amptman2077@hotmail.com',\n",
    "'edgar8593@fastmail.es',\n",
    "'roseanne7176@ownmail.net',\n",
    "'ramirez7701@123mail.org',\n",
    "'ardell3815@mailsent.net',\n",
    "'terry4639@allmail.net',\n",
    "'dale896@swift-mail.com',\n",
    "'erich_cowan3404@bestmail.us',\n",
    "'agueda4209@mm.st'\n",
    "]\n",
    "\n",
    "email_provider_list = []\n",
    "\n",
    "for email in email_address_list:\n",
    "    # split email by @, this return a list with two items\n",
    "    email_splitted_list = email.split('@')\n",
    "    \n",
    "    # take the second item as this contains the provider\n",
    "    email_second_part = email_splitted_list[1]\n",
    "\n",
    "    # then, split this part by '.' to seperate the provider from '.com'\n",
    "    email_second_splitted = email_second_part.split('.')\n",
    "    email_provider = email_second_splitted[0]\n",
    "\n",
    "    # append item to new list\n",
    "    email_provider_list.append(email_provider)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### The list with customer data"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "You have received a list with the personal data of new customers. For each customer, the first name, age and purchased product is stored in a list.\n",
    "1. Use the correct indices to write the following sentence for customer 3:\n",
    "\"{first name} is {age} years old and has bought {product}\".\n",
    "\n",
    "2. Use a for loop to iterate through all customers and print \n",
    "\"{first name} is {age} years old and has bought {product}\".\n",
    "for each of them\n",
    "\n",
    "3. Iterate through all customers and print \"Customer number {index}: {first name} is {age} years old and has bought {product}\"."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [],
   "source": [
    "# pay attention! this is a list of lists...\n",
    "\n",
    "customers = [['Paul', 33, 'Macbook Pro'],\n",
    "            ['Anna', 12, 'Looping Louie'],\n",
    "            ['Gina', 85, 'Photo Album'],\n",
    "            ['Kim', 59, 'Plants']]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Gina is 85 years old and has bought Photo Album.\n"
     ]
    }
   ],
   "source": [
    "#1.\n",
    "print(f'{customers[2][0]} is {customers[2][1]} years old and has bought {customers[2][2]}.')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "#2. \n",
    "for customer in customers:\n",
    "    print((f'{customer[0]} is {customer[1]} years old and has bought {customer[2]}.'))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "#3. \n",
    "for idx, customer in enumerate(customers):\n",
    "    print(f'Customer number {idx+1}: {customer[0]} is {customer[1]} years old and has bought {customer[2]}.')"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "nf_base",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.10.13"
  },
  "orig_nbformat": 4
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
