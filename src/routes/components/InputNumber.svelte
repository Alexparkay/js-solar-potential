<!--
 Copyright 2023 Google LLC

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
 -->

<script lang="ts">
  import type { MdOutlinedTextField } from '@material/web/textfield/outlined-text-field';

  export let icon: string;
  export let label: string;
  export let value = 0;
  export let min: number | undefined = undefined;
  export let max: number | undefined = undefined;
  export let step: number | undefined = undefined;
  export let prefix: string | undefined = undefined;
  export let suffix: string | undefined = undefined;
  export let put: (x: number) => string = (x) => x.toString();
  export let get: (x: number) => number = (x) => x;
  export let onChange: (x: number) => void = () => {};

  function _onChange(event: Event) {
    const target = event.target as MdOutlinedTextField;
    value = get(Number(target.value));
    onChange(value);
  }
</script>

<md-outlined-text-field
  type="number"
  {label}
  value={put(value)}
  {min}
  {max}
  step={step}
  prefix-text={prefix}
  suffix-text={suffix}
  on:change={_onChange}
  class="text-white"
>
  <md-icon slot="leadingicon" class="text-white">{icon}</md-icon>
</md-outlined-text-field>

<style>
  /* Override Material Web Components styles to ensure text is black */
  :global(md-outlined-text-field) {
    --md-sys-color-on-surface: #000000;
    --md-sys-color-on-surface-variant: #000000;
    --md-sys-color-outline: #000000;
    --md-sys-color-primary: #000000;
    --md-outlined-text-field-input-text-color: #000000;
    --md-outlined-text-field-label-text-color: #000000;
    --md-outlined-text-field-outline-color: rgba(0, 0, 0, 0.6);
    --md-outlined-text-field-hover-outline-color: rgba(0, 0, 0, 0.8);
    --md-outlined-text-field-focus-outline-color: #000000;
    --md-outlined-text-field-caret-color: #000000;
  }

  :global(md-outlined-text-field input) {
    color: #000000 !important;
  }

  :global(md-outlined-text-field .prefix-text),
  :global(md-outlined-text-field .suffix-text) {
    color: #000000 !important;
  }
</style>
