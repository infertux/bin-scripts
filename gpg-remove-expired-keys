#!/bin/bash

expired_keys="$(gpg --list-keys --fixed-list-mode --with-colons | grep "^pub:e:" | cut -f5 -d":")"

for key in $expired_keys; do
    gpg --list-keys $key
    gpg --no-greeting --delete-key $key # will ask for confirmation
    echo
done

