# 0x17. C - Doubly linked lists

## Overview
This repository contains solutions for the tasks related to doubly linked lists in C. The project is part of the Alx Software Engineering program. The tasks cover various operations on doubly linked lists, including printing, getting the length, adding nodes, deleting nodes, and more.

## Table of Contents
1. [Print List](#print-list)
2. [List Length](#list-length)
3. [Add Node](#add-node)
4. [Add Node at End](#add-node-at-end)
5. [Free List](#free-list)
6. [Get Node at Index](#get-node-at-index)
7. [Sum List](#sum-list)
8. [Insert at Index](#insert-at-index)
9. [Delete at Index](#delete-at-index)
10. [Crackme4](#crackme4)
11. [Palindromes](#palindromes)
12. [Crackme5 Keygen](#crackme5-keygen)

## Print List
### Task:
Write a function that prints all the elements of a dlistint_t list.
```c
size_t print_dlistint(const dlistint_t *h);
```
- Returns: the number of nodes
- Format: see example

## List Length
### Task:
Write a function that returns the number of elements in a linked dlistint_t list.
```c
size_t dlistint_len(const dlistint_t *h);
```

## Add Node
### Task:
Write a function that adds a new node at the beginning of a dlistint_t list.
```c
dlistint_t *add_dnodeint(dlistint_t **head, const int n);
```
- Returns: the address of the new element, or NULL if it failed

## Add Node at End
### Task:
Write a function that adds a new node at the end of a dlistint_t list.
```c
dlistint_t *add_dnodeint_end(dlistint_t **head, const int n);
```
- Returns: the address of the new element, or NULL if it failed

## Free List
### Task:
Write a function that frees a dlistint_t list.
```c
void free_dlistint(dlistint_t *head);
```

## Get Node at Index
### Task:
Write a function that returns the nth node of a dlistint_t linked list.
```c
dlistint_t *get_dnodeint_at_index(dlistint_t *head, unsigned int index);
```
- Returns: the address of the nth node, or NULL if the node does not exist

## Sum List
### Task:
Write a function that returns the sum of all the data (n) of a dlistint_t linked list.
```c
int sum_dlistint(dlistint_t *head);
```
- Returns: the sum of all data in the list

## Insert at Index
### Task:
Write a function that inserts a new node at a given position in a dlistint_t list.
```c
dlistint_t *insert_dnodeint_at_index(dlistint_t **h, unsigned int idx, int n);
```
- Returns: the address of the new node, or NULL if it failed

## Delete at Index
### Task:
Write a function that deletes the node at index index of a dlistint_t linked list.
```c
int delete_dnodeint_at_index(dlistint_t **head, unsigned int index);
```
- Returns: 1 if successful, -1 if the node does not exist or if deletion fails

## Crackme4
### Task:
Find the password for crackme4 and save it in the file `100-password`. The program prints "OK" when the correct password is provided.

## Palindromes
### Task:
Find the largest palindrome made from the product of two 3-digit numbers and save the result in the file `102-result`.

## Crackme5 Keygen
### Task:
Write a keygen for crackme5. The keygen should be used as `./keygen5 username` and print a valid key for the given username. The correct key should allow running the crackme5 program without a segmentation fault.

Feel free to explore each task's specific code file in the repository for detailed implementations.

*Note: The original code files, main.c files, and additional files for testing are available in the GitHub repository.*
