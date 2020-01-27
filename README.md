# myindigo
An indigo modified theme

Clone the theme repository:

git clone https://github.com/Riadlx/myindigo.git


Render your theme:

tutor config render --extra-config ./indigo/config.yml ./indigo/theme "$(tutor config printroot)/env/build/openedx/themes/indigo"


Rebuild the Openedx docker image:

tutor images build openedx

Restart your platform:

tutor local start -d

You will then have to enable the "indigo" theme, as per the official documentation (starting from step 3).
Customization

A few settings in the theme can be easily customised: this includes the theme primary color, landing page tagline, footer legal links. Theme settings are defined in the config.yml file at the root of the repository. You can override all or part of those settings by creating you own config-custom.yml file. Then, render the theme with:

tutor config render \
    --extra-config ./indigo/config.yml \
    --extra-config ./indigo/config-custom.yml \
    ./indigo/theme "$(tutor config printroot)/env/build/openedx/themes/indigo"

License

This work is licensed under the terms of the GNU Affero General Public License (AGPL).

