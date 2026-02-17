# Token Governance (reference snippet)

This document references the ERC-20 style token governance snippet used as example governance artifact. It documents the key invariants and behaviors.

Excerpt (representative):

function totalSupply() public view returns (uint256) { return _totalSupply; }
function balanceOf(address account) public view returns (uint256) { return _balances[account]; }

function transfer(address to, uint256 amount) public returns (bool) { _transfer(msg.sender, to, amount); return true; }

function approve(address spender, uint256 amount) public returns (bool) { _approve(msg.sender, spender, amount); return true; }

function transferFrom(address from, address to, uint256 amount) public returns (bool) { _spendAllowance(from, msg.sender, amount); _transfer(from, to, amount); return true; }

Internal engine functions: _transfer, _mint, _approve, _spendAllowance (see on-chain contract for definitive source).

Governance notes:
- totalSupply is a global monetary invariant.
- approvals represent delegated sovereignty and require caution for race conditions.
