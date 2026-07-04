**Blade Templates and how they work:**


Blade template is a way to make writing php on views folder  easier for developers 

Allows writing conditions as `@if,@foreach,{{$variable}}` and laravel translate it into php code .

**Example**

```
@if ($ideas->count())-->blade template

    <div class="mt-6 text-white">

        <h2 class="font-bold">Your Ideas</h2>

  

        <ul class="mt-6">

            @foreach($ideas as $idea)

                <li class="text-sm">{{ $idea->description }}</li>

            @endforeach

        </ul>

    </div>

@endif ->blade template
```
---
**2-What is the ORM, and why is it so useful**

ORM : is a way to deal with database easily without writing a formal query.

it's like using `all(),create`

**Example**
```
$ideas = Idea::where('state','pending')->get();
```
---
**Facade Design Pattern and how Laravel Use it**

Is a way to avoid repeating complex steps by making a folder contains this steps ,it helps avoiding rewriting this complicated steps.


**Example**

```
<?php
use Illuminate\Support\Facades\Route;

use App\Models\Idea;

Route::get('/', function () {

    $ideas = Idea::where('state','pending')->get();

    return view('ideas', [

        'ideas' => $ideas

    ]);

});

Route::post('/ideas', function () {

    Idea::create([

        'content' => request('idea'),

    ]);

    return redirect('/');

});
```
---
**Factory Design Pattern**

---
**Solid Principles**

**1-Single Responsibility Principle**

This means that each function should have only one job no more than it .

**Example**
writing a function that gives the developer all names in database and all function job is to do that 
```
public function getAllUsersNames()
 $names = DB::table('users')->get('name');
```
**2-Open/Closed Principle**

This means that every entity can be extended without any change or modification.

**3. Liskov's Substitution Principle**

this means that for every child class,it can be replaced (put the child class instead of parent class)
without any strange behaviour.


**4. Interface Segregation Principle**

This means preventing the behaviour of making all code related to each other, each change require changing in many parts.
But, Having an interface (simple) for each controller is the est way.


**5-Dependency Inversion Principle**

Means preventing high level modules  depend on low-level modules.
The right direction is to make both (high level modules and low-level modules) depend on general ideas.
