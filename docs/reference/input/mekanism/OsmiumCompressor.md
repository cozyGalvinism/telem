---
telem:
  adapter:
    id: 'osmiumCompressor'
    name: 'Osmium Compressor'
    categories: '{ "basic", "advanced", "input", "energy", "recipe" }'
---

<script setup>
  import { data as metrics } from './common/metrics.data.ts'
</script>

# Mekanism Osmium Compressor Input <RepoLink path="lib/input/mekanism/OsmiumCompressorInputAdapter.lua" />

<!--@include: ./common/preamble.md -->

### Basic

<MetricTable
  prefix="mekcompress:"
  :metrics="[
    { name: 'chemical_filled_percentage', value: '0.0 - 1.0'                },
    { name: 'input_count',                value: '0 - inf',   unit: 'item'  },
    { name: 'chemical_item_count',        value: '0 - inf',   unit: 'item'  },
    { name: 'output_count',               value: '0 - inf',   unit: 'item'  },
    { name: 'energy_usage',               value: '0.0 - inf', unit: 'FE/t'  },
    ...metrics.genericMachine.basic
  ]"
/>

### Advanced

<MetricTable
  prefix="mekcompress:"
  :metrics="[
    ...metrics.genericMachine.advanced
  ]"
/>

### Input

<MetricTable
  prefix="mekcompress:"
  :metrics="[
    { name: 'chemical',           value: '0.0 - inf', unit: 'B' },
    { name: 'chemical_capacity',  value: '0.0 - inf', unit: 'B' },
    { name: 'chemical_needed',    value: '0.0 - inf', unit: 'B' }
  ]"
/>

### Energy

<MetricTable
  prefix="mekcompress:"
  :metrics="[
    ...metrics.genericMachine.energy
  ]"
/>

### Recipe

<MetricTable
  prefix="mekcompress:"
  :metrics="[
    ...metrics.recipeProgress.recipe,
  ]"
/>