Remember Me
===========

Save entries for a user during a session. This could be used for a 'add to cart' function or for a 'product compare' function (save entry_id's for later use). Entries are only stored during a session.

Remember Me is an ExpressionEngine 1.x add-on.


Usage
-----

  // Save entry to storage
  {exp:remember_me:set entry_id='61'}

  // Get all entries from storage
  {exp:remember_me:get}

  // Get entries belonging to a certain channel from storage
  {exp:remember_me:get channel='producten'}<br />

  // Check if a certain entry is in storage
  {if {exp:remember_me:get entry_id='61'}}
    Entry in storage
  {if:else}
    Entry not in storage
  {/if}

  // Clear entire storage
  {exp:remember_me:clear}

  // Remove single entry from storage
  {exp:remember_me:clear entry_id='61'}

  // Remove entries belonging to a certain channel from storage
  {exp:remember_me:clear channel='products'}

  // It can also be used in conjunction with the {exp:weblog:entries} loop
  {exp:weblog:entries entry_id="{exp:remember_me:get channel='producten' parse='inward'}" parse='inward' dynamic='off'}
    {title}<br />
  {/exp:weblog:entries}