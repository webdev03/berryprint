<script lang="ts">
  import { enhance } from '$app/forms';
  import type { ActionData } from './$types';

  let { form }: { form: ActionData } = $props();
</script>

<h1>Login</h1>
<form method="post" action="?/login" use:enhance>
  <label>
    Username
    <input name="username" class="form-control" />
  </label>
  <label>
    Password
    <input type="password" name="password" class="form-control" />
  </label>
  <button class="btn btn-primary">Login</button>
</form>
<p style="color: red">{form?.message ?? ''}</p>
