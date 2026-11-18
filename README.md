# KrestyAC (Paper 1.21.11, Java 21+ / 25)

## Derleme
JDK 25 + Maven kurulu olmali:

    mvn clean package

Jar: `target/KrestyAC.jar` -> sunucunun `plugins/` klasorune at.

## Moduller
- Killaura: reach, bakis acisi, coklu hedef, CPS
- Fly: hover + surekli yukselme
- AutoTotem: totem patlayinca <90ms icinde geri takma
- Crystal macro: yerlestir->kir ayni tick + asiri duzenli ritim
- Anchor macro: charge->explode ayni tick
- Speed (10 tick toplam mesafe), NoFall (sahte yerdeyim), Scaffold (pitch + hiz)

Tum esikler, ban gunleri (15-30) ve mesajlar `config.yml` icinde.
Komut: `/kac reload`. Yetkili bildirimi: `krestyaac.alerts`. Muaf: `krestyaac.bypass`.

## Base / Storage ESP
Bu bir anticheat isi degil. `config/paper-world-defaults.yml`:

    anticheat:
      anti-xray:
        enabled: true
        engine-mode: 2
        hidden-blocks:
          - chest
          - trapped_chest
          - barrel
          - ender_chest
          - furnace
          - blast_furnace
          - shulker_box
          - hopper
          - dispenser
          - dropper
        max-block-height: 64

Not: Anti-xray sadece havaya acik olmayan (gomulu) bloklari gizler.
Yuzeydeki base'ler gizlenemez.

## Ilk kurulum onerisi
Ilk 2-3 gun `punish: false` yap, alertlere bak, false flag cikmiyorsa `true` yap.
