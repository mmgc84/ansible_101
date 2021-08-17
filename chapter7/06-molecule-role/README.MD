# Molecule testing

Create a new role with molecule

    molecule init role myrole --driver-name docker

Then test it:

    molecule test

And test it but leave the container running for debugging:

    molecule converge

Set a 'breakpoint' using `fail:` in the tasks.