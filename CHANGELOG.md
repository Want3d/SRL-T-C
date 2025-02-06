## 1.0.8 (2025-02-06)


### Bug Fixes

* add new bank scroll area function ([bb2789f](https://github.com/Want3d/SRL-T-C/commit/bb2789f712aa2b8bfe856af96fe879b3465b2854))
* add new chat scroll area ([6412fa5](https://github.com/Want3d/SRL-T-C/commit/6412fa5573aa9e3b91cdd2be7076738120f0bdda))
* attempt to fix login docs ([#75](https://github.com/Want3d/SRL-T-C/issues/75)) ([9a6aea2](https://github.com/Want3d/SRL-T-C/commit/9a6aea23d3e06a8d80769fcc1833a9d5615fcc73))
* **Bank:** Finding item scroll position shouldn't get stuck in endless loops anymore ([8968762](https://github.com/Want3d/SRL-T-C/commit/896876253c7c1d2bc4bc77e692c5dc77d8ae95fe))
* conver all old global constants to the new ones ([0eb1619](https://github.com/Want3d/SRL-T-C/commit/0eb161934e84f69ce11ac2303854571820546b0b))
* fixed issues with GameTabs.GetCurrentTab ([cd9d6f6](https://github.com/Want3d/SRL-T-C/commit/cd9d6f63ffa02a6a7d3914e62073ed461eb89e8a))
* Inventory.FindItems was not returning the actual slots the items were in. ([1cb1396](https://github.com/Want3d/SRL-T-C/commit/1cb1396ca366c4243e56fd9c7561114dc7506d0b))
* itemfinder ([36c75ef](https://github.com/Want3d/SRL-T-C/commit/36c75effb2c3125f19c260c19669f8b299c4a0c0))
* **itemfinder:** fixed noted items ([094b89f](https://github.com/Want3d/SRL-T-C/commit/094b89f3cf0356a652ffe0158f338dbb08adbdb0))
* magic tab detection ([ea19aae](https://github.com/Want3d/SRL-T-C/commit/ea19aae596e75c4cbf8274ed44a1612538243437))
* Make.IsOpen() in the world switcher ([#77](https://github.com/Want3d/SRL-T-C/issues/77)) ([bd478f5](https://github.com/Want3d/SRL-T-C/commit/bd478f5b79dee7e1988765ae4c3a01aa290039c7))
* read comments ([#73](https://github.com/Want3d/SRL-T-C/issues/73)) ([6f8f1a8](https://github.com/Want3d/SRL-T-C/commit/6f8f1a8a66206c58657445a695a4afe4af3cfd0e))
* scroll area ([0977885](https://github.com/Want3d/SRL-T-C/commit/097788501b9acabcdf15cf716e63b9c847ceec39))
* stop crashes from checking tabs when they are not available ([4724a18](https://github.com/Want3d/SRL-T-C/commit/4724a188446c9f66123af7b15b6c928fceef28ce))
* TRSBank.IsOpen() ([#76](https://github.com/Want3d/SRL-T-C/issues/76)) ([c9dd656](https://github.com/Want3d/SRL-T-C/commit/c9dd65605df07a889a707911178533e92f70c204))
* TRSLogin, Loginc messages and BioHash ([#69](https://github.com/Want3d/SRL-T-C/issues/69)) ([7864b43](https://github.com/Want3d/SRL-T-C/commit/7864b435c8e6e7afb02f393464d5083c9f15e9e2))
* TRSMake fixes ([#68](https://github.com/Want3d/SRL-T-C/issues/68)) ([f4b1a62](https://github.com/Want3d/SRL-T-C/commit/f4b1a6269a0f0091de5621119d7d2437e41734be))
* TRSWalkerMap.GlobalToRegion() was not offsetting properly. ([#70](https://github.com/Want3d/SRL-T-C/issues/70)) ([2222beb](https://github.com/Want3d/SRL-T-C/commit/2222beb594162ee8c69517070469e5c069f2bd2d))
* update docs link ([e85e2fd](https://github.com/Want3d/SRL-T-C/commit/e85e2fdf90b960272621715c83a176b846fb9a35))
* update item-finder ([4130cf5](https://github.com/Want3d/SRL-T-C/commit/4130cf587705549e10fa0cb8bc604f46375a30dc))
* update remoteinput plugin ([ec1f4e9](https://github.com/Want3d/SRL-T-C/commit/ec1f4e93b32a664cb38b47e5cac266c22dd74a36))


* Bug fixes and minor additions (#65) ([0e9d699](https://github.com/Want3d/SRL-T-C/commit/0e9d69914cafa0e7089ca9eb2bd95febbb069505)), closes [#65](https://github.com/Want3d/SRL-T-C/issues/65)


### Features

* add TRSBankItem ([e94fe3a](https://github.com/Want3d/SRL-T-C/commit/e94fe3a4312f3e325343536c021dc83733840ef7))
* **bank:** methods to find bank tabs a item is in ([19a335b](https://github.com/Want3d/SRL-T-C/commit/19a335b85a7d4327f542167fff5724fd4ce56b2c))
* fixed zoom slider and added brightness slider ([f65bc17](https://github.com/Want3d/SRL-T-C/commit/f65bc17a9d9cfb93a5b76ffa3ff072c44e92c3cf))
* new keybindings.simba file to handle FKeys. ([8fd288d](https://github.com/Want3d/SRL-T-C/commit/8fd288d85da40aa2b9725ca92b033806305c653f))


### BREAKING CHANGES

* This breaks compatibility with old SRL scripts that used the updated methods because what used to be passed as **roll** is not something else.
* `TRSMainScreen.ConvertDistance()` was renamed to `TRSMainScreen.NormalizeDistance()`.
				 This was renamed by Olly in Simba1500, I guess it's an optional change but I think the rename
				 makes sense and since we are breaking compatibility, might as well bring things closer to 1500
				 already so people have less headaches later.
				 We could also optionally keep both methods and mark this one as deprecated. I'll wait for your feedback.
				 P.S. The method was actually rewrotten in 1500 but was not worth backporting, so I just renamed it!

* fix: update `MainScreen.ConvertDistance()` references to `MainScreen.NormalizeDistance()`

* refactor: added `Contains` methods to equipment and inventory.

I've also left a comment on the PR after the last commit because I forgot to mention TRSBank.ContainsItem().

Anyway, this has the same reasoning. This is optional but I would like to bring the SRL1400 API closer to SRL1500 API.

Old methods are kept and marked with a comment as deprecated so there's no downside to adding this.

This also brings documentation to TRSInventory which is nice :)

* fix: added deprecated warnings

also added more docs to inventory

* fix: added delay after mouse drag release



