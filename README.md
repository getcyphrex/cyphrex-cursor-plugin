# Cyphrex for Cursor

This plugin connects Cursor to Cyphrex. Before an agent touches secrets, money, production data, a deploy, or an external send, it checks that action with Cyphrex and can read the audit log afterward.

The theme is: Don't trust the agent. Verify it.

## What you get

- An MCP connection to the hosted Cyphrex server at `https://mcp.cyphrex.io/mcp`.
- A rule that applies in every session.
- A skill, `verify-the-agent`, that says when to register an agent, check an action, and pull the audit log.

## Install

This folder is the plugin. In Cursor, install it from the Marketplace when it is listed, or load this directory as a local plugin while reviewing it.

## Set CYPHREX_API_KEY

The plugin does not contain a key. After install, open Plugins, then Configure, and set `CYPHREX_API_KEY` to your Cyphrex API key.

Cursor sends that value as the `Authorization: Bearer` header on the MCP connection. Leave the value out of git, chat, and source files.

## Trial

Start a 2-week free trial at https://cyphrex.io/plans.
