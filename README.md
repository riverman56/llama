<h1 align="center">📚 Llama 🦙</h1>
<div align="center">
	<a href="https://github.com/F-RDY/llama/actions"><img src="https://github.com/F-RDY/llama/workflows/CI/badge.svg" alt="GitHub Actions Build Status" /></a>
	<a href="https://f-rdy.github.io/llama"><img src="https://img.shields.io/badge/docs-website-green.svg" alt="Documentation" /></a>
</div>
<div align="center">
	Lua Library for Immutable Data
</div>

## Installation

There are a few ways to get started with Llama.

### Method 1: Import model file

1. Download the `.rbxmx` model file from the latest release on the [Llama releases page](https://github.com/F-RDY/llama/releases).
2. Insert the model anywhere in a Roblox place!

### Method 2: Good ol' copy + paste

1. Copy the `src` directory of Llama into your project.
2. Rename it to `Llama`.
3. Use something like [Rojo](https://github.com/rojo-rbx/rojo) to sync your project to Roblox Studio!

### Method 3: Git submodule

1. Navigate to where you want to keep your submodules in Git bash.
2. Run `git submodule add https://github.com/F-RDY/llama.git`.
3. Using something like [Rojo](https://github.com/rojo-rbx/rojo), set up your project to sync `Llama/src` into Roblox Studio!

### Method 4: Package manager

*Coming Soon™*

## Usage

### Basic usage

To use Llama, simply require it as a module from where you installed it! It is also recommended that you set `Llama.Dictionary`, `Llama.List`, and `Llama.Set` to their own variables; otherwise, you'll be typing a lot!

```lua
-- Other modules...
local Llama = require(LlamaPath)

local Dictionary = Llama.Dictionary
local List = Llama.List
local Set = Llama.Set
```

### Usage with [Roact](https://github.com/Roblox/roact/) and [Rodux](https://github.com/Roblox/rodux)

Rodux requires your state to be immutable, so Llama is a great choice for manipulating it!

```lua
local function reducer(state, action)
	if action.type == "Add" then
		return Dictionary.merge(state, {
			counter = counter + 1
		})
	elseif action.type == "Subtract" then
		return Dictionary.merge(state, {
			counter = counter - 1
		})
	end
end
```

Visit the [docs](https://f-rdy.github.io/llama/) for examples and API reference.

## What's in a name?
Llamas are members of the Camelid group of mammals along with alpacas, camels, and dromedarys, which are known for being very stubborn but reliable animals.