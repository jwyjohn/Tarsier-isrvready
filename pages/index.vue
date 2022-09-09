<template>
  <v-row justify="center">
    <v-col cols="12" sm="12" md="12">
      <v-card class="logo py-4 d-flex justify-center" :elevation="0">
        <RiscvLogo />
      </v-card>
      <v-card class="logo py-4 d-flex justify-center" elevation="0">
        <v-card-title class="text-h1">
          Is RISC-V Ready
        </v-card-title>
      </v-card>
    </v-col>
    <v-col cols="6" sm="6" md="6">
      <v-text-field class="text-h5" v-model="search" label="Search" solo prepend-inner-icon="mdi-magnify">
      </v-text-field>
    </v-col>
    <v-col cols="10" sm="10" md="10">
      <v-data-table :search="search" :headers="headers" :items="bj67" multi-sort
        class="elevation-1">
        <template v-slot:item.actions="{ item }">
          <v-btn icon href="https://github.com/isrc-cas/tarsier-meta/blob/main/roadmap/checklist.md">
            <v-icon small>mdi-chevron-right</v-icon>
          </v-btn>
        </template>
      </v-data-table>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      search: '',
      headers: [
        {
          text: 'Package',
          align: 'start',
          value: 'package',
        },
        { text: 'Arch', value: 'arch', filterable: false },
        { text: 'Debian', value: 'debian', filterable: false },
        { text: 'Fedora', value: 'fedora', filterable: false },
        { text: 'OpenEuler', value: 'openeuler', filterable: false },
        { text: 'Ubuntu', value: 'ubuntu', filterable: false },
        { text: 'Last update', value: 'ludate', filterable: false },
        { text: '', align: 'start', value: 'actions', sortable: false, filterable: false },
      ],
      bj67: [
        {
          "arch": "\u26a0\ufe0f 7.7.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.4.1",
          "openeuler": "\u26a0\ufe0f 6.4.3",
          "ubuntu": "\u2705 8.4.3",
          "package": "[fake] abs-guide",
          "ludate": "2021-12-23"
        },
        {
          "arch": "\u26a0\ufe0f 9.2.5",
          "debian": "\u26a0\ufe0f 1.4.8",
          "fedora": "\u2705 2.1.9",
          "openeuler": "\u26a0\ufe0f 9.4.3",
          "ubuntu": "\u2705 6.2.6",
          "package": "[fake] album",
          "ludate": "2019-10-8"
        },
        {
          "arch": "\u2705 1.2.3",
          "debian": "\u26a0\ufe0f 2.6.9",
          "fedora": "\u26a0\ufe0f 9.5.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] album-data",
          "ludate": "2019-8-11"
        },
        {
          "arch": "\u2705 9.7.8",
          "debian": "\u2705 2.6.8",
          "fedora": "\u26a0\ufe0f 3.6.6",
          "openeuler": "\u2705 7.1.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] alien-arena-data",
          "ludate": "2019-10-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.6.6",
          "openeuler": "\u2705 7.2.5",
          "ubuntu": "\u2705 2.5.1",
          "package": "[fake] amoeba-data",
          "ludate": "2020-1-10"
        },
        {
          "arch": "\u2705 7.7.8",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 6.8.9",
          "openeuler": "\u2705 3.3.7",
          "ubuntu": "\u26a0\ufe0f 9.8.6",
          "package": "[fake] arb-common",
          "ludate": "2019-5-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.3.6",
          "fedora": "\u26a0\ufe0f 2.4.4",
          "openeuler": "\u26a0\ufe0f 3.2.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] arb-doc",
          "ludate": "2019-11-24"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.6.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] aseba-plugin-blockly",
          "ludate": "2021-6-14"
        },
        {
          "arch": "\u2705 2.2.4",
          "debian": "\u26a0\ufe0f 2.1.4",
          "fedora": "\u2705 7.9.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.4.9",
          "package": "[fake] assaultcube-data",
          "ludate": "2019-8-11"
        },
        {
          "arch": "\u2705 1.3.4",
          "debian": "\u2705 5.1.1",
          "fedora": "\u2705 9.4.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.6.9",
          "package": "[fake] astromenace-data-src",
          "ludate": "2019-10-26"
        },
        {
          "arch": "\u26a0\ufe0f 8.4.2",
          "debian": "\u26a0\ufe0f 5.5.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] astrometry-data-2mass",
          "ludate": "2019-12-16"
        },
        {
          "arch": "\u26a0\ufe0f 7.8.7",
          "debian": "\u26a0\ufe0f 8.2.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.8.5",
          "ubuntu": "\u2705 8.3.7",
          "package": "[fake] astrometry-data-2mass-00",
          "ludate": "2020-10-22"
        },
        {
          "arch": "\u2705 8.3.2",
          "debian": "\u2705 2.8.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.2.4",
          "package": "[fake] astrometry-data-2mass-01",
          "ludate": "2019-7-16"
        },
        {
          "arch": "\u26a0\ufe0f 8.6.5",
          "debian": "\u2705 1.1.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.9.6",
          "ubuntu": "\u26a0\ufe0f 9.5.8",
          "package": "[fake] astrometry-data-2mass-02",
          "ludate": "2020-12-8"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.4.3",
          "fedora": "\u2705 1.9.1",
          "openeuler": "\u2705 5.7.7",
          "ubuntu": "\u2705 7.5.3",
          "package": "[fake] astrometry-data-2mass-03",
          "ludate": "2020-11-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.4.1",
          "fedora": "\u26a0\ufe0f 1.4.8",
          "openeuler": "\u2705 4.9.1",
          "ubuntu": "\u2705 5.4.8",
          "package": "[fake] astrometry-data-2mass-04",
          "ludate": "2020-6-13"
        },
        {
          "arch": "\u26a0\ufe0f 7.7.3",
          "debian": "\u26a0\ufe0f 2.8.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.9.7",
          "package": "[fake] astrometry-data-2mass-05",
          "ludate": "2020-6-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.8.7",
          "openeuler": "\u26a0\ufe0f 6.6.2",
          "ubuntu": "\u2705 3.9.2",
          "package": "[fake] astrometry-data-2mass-06",
          "ludate": "2021-6-25"
        },
        {
          "arch": "\u2705 1.6.4",
          "debian": "\u26a0\ufe0f 4.8.1",
          "fedora": "\u26a0\ufe0f 1.8.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 6.9.3",
          "package": "[fake] astrometry-data-2mass-07",
          "ludate": "2020-3-1"
        },
        {
          "arch": "\u2705 1.9.6",
          "debian": "\u2705 7.1.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.7.6",
          "package": "[fake] astrometry-data-2mass-08-19",
          "ludate": "2021-2-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.6.8",
          "fedora": "\u26a0\ufe0f 2.9.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.4.8",
          "package": "[fake] atmel-firmware",
          "ludate": "2020-1-21"
        },
        {
          "arch": "\u26a0\ufe0f 9.2.3",
          "debian": "\u2705 7.4.5",
          "fedora": "\u2705 2.3.3",
          "openeuler": "\u2705 3.4.8",
          "ubuntu": "\u26a0\ufe0f 8.3.5",
          "package": "[fake] beast-mcmc",
          "ludate": "2021-11-5"
        },
        {
          "arch": "\u2705 4.4.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.3.3",
          "openeuler": "\u26a0\ufe0f 4.6.6",
          "ubuntu": "\u26a0\ufe0f 4.3.9",
          "package": "[fake] beast-mcmc-examples",
          "ludate": "2020-2-7"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.2.2",
          "fedora": "\u2705 1.7.3",
          "openeuler": "\u2705 5.3.9",
          "ubuntu": "\u26a0\ufe0f 5.5.5",
          "package": "[fake] bgoffice-dict-downloader",
          "ludate": "2020-2-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.6.6",
          "fedora": "\u2705 5.3.2",
          "openeuler": "\u26a0\ufe0f 2.8.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] bluez-firmware",
          "ludate": "2020-1-2"
        },
        {
          "arch": "\u2705 2.7.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.6.6",
          "ubuntu": "\u26a0\ufe0f 8.1.1",
          "package": "[fake] broadcom-sta-common",
          "ludate": "2020-11-1"
        },
        {
          "arch": "\u26a0\ufe0f 3.1.9",
          "debian": "\u26a0\ufe0f 9.1.9",
          "fedora": "\u26a0\ufe0f 1.5.6",
          "openeuler": "\u2705 6.3.9",
          "ubuntu": "\u2705 7.5.1",
          "package": "[fake] broadcom-sta-dkms",
          "ludate": "2020-12-11"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.8.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.8.8",
          "package": "[fake] broadcom-sta-source",
          "ludate": "2020-3-24"
        },
        {
          "arch": "\u2705 5.5.6",
          "debian": "\u2705 2.8.2",
          "fedora": "\u2705 8.8.4",
          "openeuler": "\u2705 1.5.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] cclib-data",
          "ludate": "2019-5-22"
        },
        {
          "arch": "\u2705 8.2.6",
          "debian": "\u26a0\ufe0f 9.1.8",
          "fedora": "\u2705 2.1.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.1.6",
          "package": "[fake] cim-schema",
          "ludate": "2019-12-6"
        },
        {
          "arch": "\u26a0\ufe0f 2.8.5",
          "debian": "\u2705 5.2.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] cl-sql-oracle",
          "ludate": "2021-11-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.3.6",
          "fedora": "\u2705 5.6.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] cl-umlisp",
          "ludate": "2021-8-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.1.1",
          "fedora": "\u2705 7.4.6",
          "openeuler": "\u26a0\ufe0f 4.7.3",
          "ubuntu": "\u26a0\ufe0f 2.7.6",
          "package": "[fake] cl-umlisp-orf",
          "ludate": "2019-3-28"
        },
        {
          "arch": "\u2705 1.4.9",
          "debian": "\u2705 3.2.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.2.4",
          "ubuntu": "\u2705 8.4.2",
          "package": "[fake] cltl",
          "ludate": "2019-1-4"
        },
        {
          "arch": "\u26a0\ufe0f 2.8.4",
          "debian": "\u26a0\ufe0f 4.2.6",
          "fedora": "\u2705 8.6.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 2.8.6",
          "package": "[fake] context-nonfree",
          "ludate": "2020-1-12"
        },
        {
          "arch": "\u2705 4.9.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 7.4.3",
          "openeuler": "\u2705 9.4.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] coq-doc",
          "ludate": "2021-12-7"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 5.9.9",
          "openeuler": "\u26a0\ufe0f 7.1.1",
          "ubuntu": "\u26a0\ufe0f 5.3.6",
          "package": "[fake] coq-doc-html",
          "ludate": "2021-10-20"
        },
        {
          "arch": "\u2705 5.7.1",
          "debian": "\u2705 5.3.6",
          "fedora": "\u26a0\ufe0f 7.7.4",
          "openeuler": "\u26a0\ufe0f 7.6.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] coq-doc-pdf",
          "ludate": "2021-1-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.8.4",
          "fedora": "\u2705 9.7.4",
          "openeuler": "\u26a0\ufe0f 8.9.8",
          "ubuntu": "\u26a0\ufe0f 9.5.4",
          "package": "[fake] corsix-th-data",
          "ludate": "2020-1-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 5.7.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.7.8",
          "package": "[fake] cpio-doc",
          "ludate": "2019-7-8"
        },
        {
          "arch": "\u26a0\ufe0f 7.8.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.2.4",
          "ubuntu": "\u2705 5.7.8",
          "package": "[fake] crafty-bitmaps",
          "ludate": "2021-12-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.9.8",
          "openeuler": "\u26a0\ufe0f 9.7.6",
          "ubuntu": "\u26a0\ufe0f 6.7.1",
          "package": "[fake] crafty-books-medium",
          "ludate": "2020-4-20"
        },
        {
          "arch": "\u2705 7.9.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.5.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.2.9",
          "package": "[fake] crafty-books-medtosmall",
          "ludate": "2020-11-11"
        },
        {
          "arch": "\u2705 3.1.6",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.8.4",
          "ubuntu": "\u2705 3.8.9",
          "package": "[fake] crafty-books-small",
          "ludate": "2019-7-23"
        },
        {
          "arch": "\u2705 9.9.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.2.8",
          "openeuler": "\u26a0\ufe0f 7.1.2",
          "ubuntu": "\u2705 7.3.3",
          "package": "[fake] cuneiform-common",
          "ludate": "2021-12-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.1.9",
          "openeuler": "\u2705 8.9.8",
          "ubuntu": "\u2705 9.4.4",
          "package": "[fake] cytadela-data",
          "ludate": "2021-7-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 4.7.7",
          "fedora": "\u26a0\ufe0f 4.9.1",
          "openeuler": "\u2705 9.1.5",
          "ubuntu": "\u26a0\ufe0f 8.7.2",
          "package": "[fake] dahdi-firmware-nonfree",
          "ludate": "2019-4-3"
        },
        {
          "arch": "\u26a0\ufe0f 3.4.8",
          "debian": "\u26a0\ufe0f 6.8.7",
          "fedora": "\u26a0\ufe0f 1.4.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.9.6",
          "package": "[fake] devede",
          "ludate": "2020-12-10"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.2.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.1.1",
          "package": "[fake] dgen",
          "ludate": "2020-10-15"
        },
        {
          "arch": "\u2705 6.5.8",
          "debian": "\u26a0\ufe0f 4.3.4",
          "fedora": "\u26a0\ufe0f 1.6.6",
          "openeuler": "\u26a0\ufe0f 4.4.9",
          "ubuntu": "\u26a0\ufe0f 7.1.8",
          "package": "[fake] divxenc",
          "ludate": "2019-11-12"
        },
        {
          "arch": "\u2705 9.3.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] doc-rfc",
          "ludate": "2021-5-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.6.4",
          "fedora": "\u26a0\ufe0f 1.3.8",
          "openeuler": "\u26a0\ufe0f 7.4.7",
          "ubuntu": "\u2705 3.9.1",
          "package": "[fake] doc-rfc-experimental",
          "ludate": "2019-6-14"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.1",
          "debian": "\u26a0\ufe0f 4.4.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.5.8",
          "package": "[fake] doc-rfc-fyi-bcp",
          "ludate": "2020-10-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.5.7",
          "ubuntu": "\u26a0\ufe0f 9.1.6",
          "package": "[fake] doc-rfc-informational",
          "ludate": "2020-10-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.2.2",
          "ubuntu": "\u2705 7.3.1",
          "package": "[fake] doc-rfc-misc",
          "ludate": "2020-1-6"
        },
        {
          "arch": "\u2705 6.3.9",
          "debian": "\u2705 1.9.7",
          "fedora": "\u26a0\ufe0f 1.8.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 1.7.8",
          "package": "[fake] doc-rfc-old-std",
          "ludate": "2021-12-9"
        },
        {
          "arch": "\u2705 6.4.3",
          "debian": "\u2705 2.8.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 7.6.5",
          "ubuntu": "\u2705 9.3.1",
          "package": "[fake] doc-rfc-others",
          "ludate": "2021-3-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.8.8",
          "fedora": "\u2705 1.6.9",
          "openeuler": "\u26a0\ufe0f 6.7.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] doc-rfc-std",
          "ludate": "2020-3-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.9.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.3.1",
          "package": "[fake] doc-rfc-std-proposed",
          "ludate": "2020-12-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 6.5.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.7.3",
          "package": "[fake] doom-wad-shareware",
          "ludate": "2020-7-11"
        },
        {
          "arch": "\u26a0\ufe0f 2.4.4",
          "debian": "\u26a0\ufe0f 9.3.2",
          "fedora": "\u26a0\ufe0f 3.8.9",
          "openeuler": "\u2705 6.6.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] dvd-slideshow",
          "ludate": "2021-3-2"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.3.4",
          "openeuler": "\u26a0\ufe0f 4.3.3",
          "ubuntu": "\u26a0\ufe0f 9.7.7",
          "package": "[fake] dwarf-fortress-data",
          "ludate": "2020-4-9"
        },
        {
          "arch": "\u26a0\ufe0f 1.4.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.5.5",
          "openeuler": "\u2705 9.8.4",
          "ubuntu": "\u2705 3.5.8",
          "package": "[fake] dynare-matlab",
          "ludate": "2021-12-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.6.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 1.1.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] ebook-dev-alp",
          "ludate": "2021-6-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 5.2.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.1.5",
          "package": "[fake] ec2-ami-tools",
          "ludate": "2021-9-12"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 6.1.4",
          "fedora": "\u2705 5.7.9",
          "openeuler": "\u26a0\ufe0f 9.4.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] ec2-api-tools",
          "ludate": "2021-7-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.1.6",
          "openeuler": "\u26a0\ufe0f 6.1.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] emacs-common-non-dfsg",
          "ludate": "2019-2-10"
        },
        {
          "arch": "\u26a0\ufe0f 4.3.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.6.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.8.9",
          "package": "[fake] esix",
          "ludate": "2020-4-24"
        },
        {
          "arch": "\u26a0\ufe0f 7.3.1",
          "debian": "\u26a0\ufe0f 2.3.5",
          "fedora": "\u26a0\ufe0f 2.3.5",
          "openeuler": "\u26a0\ufe0f 7.6.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] etoys",
          "ludate": "2021-6-24"
        },
        {
          "arch": "\u2705 8.9.7",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 1.6.6",
          "package": "[fake] etoys-doc",
          "ludate": "2020-4-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.8.7",
          "fedora": "\u2705 8.8.5",
          "openeuler": "\u26a0\ufe0f 3.1.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] etqw",
          "ludate": "2021-5-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 4.8.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 2.8.8",
          "ubuntu": "\u26a0\ufe0f 9.3.1",
          "package": "[fake] etqw-server",
          "ludate": "2019-5-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.4.4",
          "fedora": "\u2705 5.2.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.6.3",
          "package": "[fake] fasta3-doc",
          "ludate": "2019-8-20"
        },
        {
          "arch": "\u2705 5.2.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.8.7",
          "openeuler": "\u26a0\ufe0f 5.2.9",
          "ubuntu": "\u2705 6.5.3",
          "package": "[fake] fasttracker2",
          "ludate": "2021-5-9"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.3.4",
          "fedora": "\u2705 2.5.3",
          "openeuler": "\u26a0\ufe0f 1.8.6",
          "ubuntu": "\u26a0\ufe0f 3.8.2",
          "package": "[fake] festlex-oald",
          "ludate": "2020-1-25"
        },
        {
          "arch": "\u26a0\ufe0f 1.7.6",
          "debian": "\u26a0\ufe0f 8.2.9",
          "fedora": "\u26a0\ufe0f 5.1.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 1.8.2",
          "package": "[fake] festvox-don",
          "ludate": "2021-11-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.2.8",
          "fedora": "\u2705 9.1.6",
          "openeuler": "\u26a0\ufe0f 8.8.5",
          "ubuntu": "\u2705 8.7.9",
          "package": "[fake] festvox-ellpc11k",
          "ludate": "2019-6-24"
        },
        {
          "arch": "\u26a0\ufe0f 7.6.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 6.3.5",
          "openeuler": "\u26a0\ufe0f 2.5.6",
          "ubuntu": "\u2705 9.6.6",
          "package": "[fake] festvox-en1",
          "ludate": "2020-2-26"
        },
        {
          "arch": "\u2705 3.3.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 3.2.3",
          "ubuntu": "\u2705 1.2.7",
          "package": "[fake] festvox-rablpc16k",
          "ludate": "2019-12-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.6.1",
          "package": "[fake] festvox-rablpc8k",
          "ludate": "2020-7-27"
        },
        {
          "arch": "\u2705 6.6.7",
          "debian": "\u2705 6.2.4",
          "fedora": "\u2705 5.4.7",
          "openeuler": "\u2705 9.1.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] festvox-us1",
          "ludate": "2019-6-12"
        },
        {
          "arch": "\u26a0\ufe0f 3.1.9",
          "debian": "\u2705 8.7.8",
          "fedora": "\u26a0\ufe0f 1.1.7",
          "openeuler": "\u26a0\ufe0f 6.3.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] festvox-us2",
          "ludate": "2020-12-10"
        },
        {
          "arch": "\u26a0\ufe0f 8.8.9",
          "debian": "\u26a0\ufe0f 2.5.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 6.5.1",
          "ubuntu": "\u26a0\ufe0f 9.1.9",
          "package": "[fake] festvox-us3",
          "ludate": "2021-1-8"
        },
        {
          "arch": "\u2705 3.2.3",
          "debian": "\u26a0\ufe0f 4.2.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.6.8",
          "ubuntu": "\u2705 3.6.2",
          "package": "[fake] fheroes2-pkg",
          "ludate": "2019-2-14"
        },
        {
          "arch": "\u26a0\ufe0f 2.7.4",
          "debian": "\u2705 3.9.9",
          "fedora": "\u26a0\ufe0f 4.9.4",
          "openeuler": "\u26a0\ufe0f 9.6.1",
          "ubuntu": "\u26a0\ufe0f 9.9.7",
          "package": "[fake] firmware-ast",
          "ludate": "2021-2-6"
        },
        {
          "arch": "\u26a0\ufe0f 1.7.9",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 5.5.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] firmware-b43-installer",
          "ludate": "2021-2-8"
        },
        {
          "arch": "\u26a0\ufe0f 9.9.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.9.1",
          "openeuler": "\u26a0\ufe0f 3.5.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] firmware-b43legacy-installer",
          "ludate": "2020-12-9"
        },
        {
          "arch": "\u26a0\ufe0f 3.1.7",
          "debian": "\u2705 5.6.3",
          "fedora": "\u2705 8.6.6",
          "openeuler": "\u2705 4.5.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] firmware-realtek-rtl8723cs-bt",
          "ludate": "2021-11-20"
        },
        {
          "arch": "\u2705 8.2.9",
          "debian": "\u26a0\ufe0f 9.7.5",
          "fedora": "\u26a0\ufe0f 5.5.8",
          "openeuler": "\u2705 2.8.1",
          "ubuntu": "\u2705 1.9.3",
          "package": "[fake] foiltex",
          "ludate": "2021-11-14"
        },
        {
          "arch": "\u2705 6.5.5",
          "debian": "\u26a0\ufe0f 9.3.7",
          "fedora": "\u26a0\ufe0f 5.7.7",
          "openeuler": "\u2705 8.7.6",
          "ubuntu": "\u26a0\ufe0f 1.3.2",
          "package": "[fake] fonts-cns11643-kai",
          "ludate": "2019-7-26"
        },
        {
          "arch": "\u2705 8.8.7",
          "debian": "\u26a0\ufe0f 5.9.9",
          "fedora": "\u26a0\ufe0f 4.1.5",
          "openeuler": "\u26a0\ufe0f 7.9.9",
          "ubuntu": "\u2705 3.9.9",
          "package": "[fake] fonts-cns11643-sung",
          "ludate": "2019-5-4"
        },
        {
          "arch": "\u2705 9.2.4",
          "debian": "\u2705 2.3.5",
          "fedora": "\u26a0\ufe0f 8.6.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.1.3",
          "package": "[fake] fonts-ibm-plex",
          "ludate": "2021-10-1"
        },
        {
          "arch": "\u2705 4.6.5",
          "debian": "\u26a0\ufe0f 8.4.4",
          "fedora": "\u2705 5.8.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] fonts-ipafont-nonfree-jisx0208",
          "ludate": "2019-9-10"
        },
        {
          "arch": "\u26a0\ufe0f 8.8.5",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 6.9.3",
          "package": "[fake] fonts-ipafont-nonfree-uigothic",
          "ludate": "2021-11-8"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.3.1",
          "fedora": "\u2705 8.1.3",
          "openeuler": "\u26a0\ufe0f 3.3.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] fonts-jetbrains-mono",
          "ludate": "2019-4-19"
        },
        {
          "arch": "\u2705 1.9.8",
          "debian": "\u2705 3.4.9",
          "fedora": "\u2705 3.7.7",
          "openeuler": "\u2705 5.8.6",
          "ubuntu": "\u26a0\ufe0f 4.7.8",
          "package": "[fake] fonts-larabie-deco",
          "ludate": "2019-4-23"
        },
        {
          "arch": "\u2705 8.8.6",
          "debian": "\u26a0\ufe0f 3.7.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.1.2",
          "package": "[fake] fonts-larabie-straight",
          "ludate": "2020-8-19"
        },
        {
          "arch": "\u2705 7.1.4",
          "debian": "\u2705 1.8.3",
          "fedora": "\u2705 3.4.7",
          "openeuler": "\u26a0\ufe0f 1.6.9",
          "ubuntu": "\u26a0\ufe0f 3.7.4",
          "package": "[fake] fonts-larabie-uncommon",
          "ludate": "2020-12-28"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.2",
          "debian": "\u2705 6.9.6",
          "fedora": "\u26a0\ufe0f 5.5.7",
          "openeuler": "\u26a0\ufe0f 1.6.3",
          "ubuntu": "\u26a0\ufe0f 4.6.3",
          "package": "[fake] fonts-mikachan",
          "ludate": "2021-8-3"
        },
        {
          "arch": "\u2705 5.5.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.4.4",
          "openeuler": "\u2705 8.6.4",
          "ubuntu": "\u26a0\ufe0f 1.2.8",
          "package": "[fake] fonts-moe-standard-kai",
          "ludate": "2021-2-26"
        },
        {
          "arch": "\u2705 4.8.3",
          "debian": "\u2705 2.8.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 3.5.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] fonts-moe-standard-song",
          "ludate": "2021-5-25"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.5.1",
          "openeuler": "\u26a0\ufe0f 1.9.7",
          "ubuntu": "\u2705 6.7.9",
          "package": "[fake] fonts-mononoki",
          "ludate": "2020-5-13"
        },
        {
          "arch": "\u26a0\ufe0f 9.6.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.1.8",
          "openeuler": "\u26a0\ufe0f 8.4.8",
          "ubuntu": "\u2705 5.5.6",
          "package": "[fake] fonts-xfree86-nonfree",
          "ludate": "2021-9-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 2.4.5",
          "openeuler": "\u2705 5.6.5",
          "ubuntu": "\u2705 7.9.4",
          "package": "[fake] fonts-xfree86-nonfree-syriac",
          "ludate": "2019-2-15"
        },
        {
          "arch": "\u26a0\ufe0f 3.1.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.6.4",
          "openeuler": "\u26a0\ufe0f 3.3.1",
          "ubuntu": "\u26a0\ufe0f 5.7.3",
          "package": "[fake] frogatto-data",
          "ludate": "2019-4-24"
        },
        {
          "arch": "\u2705 1.1.8",
          "debian": "\u26a0\ufe0f 5.3.7",
          "fedora": "\u2705 6.5.8",
          "openeuler": "\u2705 7.1.5",
          "ubuntu": "\u2705 2.5.9",
          "package": "[fake] game-data-packager",
          "ludate": "2021-6-1"
        },
        {
          "arch": "\u26a0\ufe0f 8.2.5",
          "debian": "\u2705 2.9.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 6.8.9",
          "package": "[fake] game-data-packager-runtime",
          "ludate": "2019-7-7"
        },
        {
          "arch": "\u26a0\ufe0f 2.7.9",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.2.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gemrb-baldurs-gate-2-data",
          "ludate": "2021-10-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.3.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gemrb-baldurs-gate-data",
          "ludate": "2019-7-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.2.2",
          "fedora": "\u26a0\ufe0f 8.5.7",
          "openeuler": "\u26a0\ufe0f 4.4.1",
          "ubuntu": "\u2705 1.1.1",
          "package": "[fake] gemrb-data",
          "ludate": "2020-8-4"
        },
        {
          "arch": "\u2705 5.2.8",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.6.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gemrb-doc",
          "ludate": "2020-12-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.7.8",
          "fedora": "\u26a0\ufe0f 7.5.3",
          "openeuler": "\u2705 1.7.9",
          "ubuntu": "\u2705 5.8.5",
          "package": "[fake] gemrb-icewind-dale-2-data",
          "ludate": "2020-9-26"
        },
        {
          "arch": "\u26a0\ufe0f 1.1.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.7.8",
          "openeuler": "\u26a0\ufe0f 6.2.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gemrb-icewind-dale-data",
          "ludate": "2021-11-13"
        },
        {
          "arch": "\u2705 2.2.9",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.1.3",
          "ubuntu": "\u2705 3.3.2",
          "package": "[fake] gemrb-planescape-torment-data",
          "ludate": "2019-2-21"
        },
        {
          "arch": "\u2705 4.1.1",
          "debian": "\u2705 3.8.2",
          "fedora": "\u26a0\ufe0f 5.3.8",
          "openeuler": "\u2705 7.6.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gfaim-data",
          "ludate": "2020-6-17"
        },
        {
          "arch": "\u26a0\ufe0f 9.9.1",
          "debian": "\u26a0\ufe0f 4.8.8",
          "fedora": "\u2705 6.1.8",
          "openeuler": "\u26a0\ufe0f 9.5.1",
          "ubuntu": "\u2705 6.7.2",
          "package": "[fake] gliese",
          "ludate": "2020-2-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.5.4",
          "ubuntu": "\u26a0\ufe0f 6.7.3",
          "package": "[fake] gmp-doc",
          "ludate": "2021-9-18"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 8.6.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gnome-shell-extension-hijra",
          "ludate": "2021-6-22"
        },
        {
          "arch": "\u2705 7.8.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.4.7",
          "openeuler": "\u2705 5.2.6",
          "ubuntu": "\u2705 5.3.7",
          "package": "[fake] google-android-cmdline-tools-1.0-installer",
          "ludate": "2020-1-8"
        },
        {
          "arch": "\u2705 1.8.4",
          "debian": "\u2705 1.2.4",
          "fedora": "\u2705 9.7.3",
          "openeuler": "\u26a0\ufe0f 3.3.1",
          "ubuntu": "\u26a0\ufe0f 9.7.1",
          "package": "[fake] google-android-cmdline-tools-2.1-installer",
          "ludate": "2021-9-3"
        },
        {
          "arch": "\u2705 5.3.4",
          "debian": "\u26a0\ufe0f 5.9.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.6.8",
          "ubuntu": "\u2705 8.3.2",
          "package": "[fake] google-android-cmdline-tools-3.0-installer",
          "ludate": "2020-5-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.5.2",
          "fedora": "\u26a0\ufe0f 1.3.2",
          "openeuler": "\u2705 5.1.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-cmdline-tools-4.0-installer",
          "ludate": "2019-3-23"
        },
        {
          "arch": "\u2705 4.2.2",
          "debian": "\u2705 8.2.7",
          "fedora": "\u2705 5.2.6",
          "openeuler": "\u2705 7.5.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-cmdline-tools-5.0-installer",
          "ludate": "2019-3-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 7.6.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.1.7",
          "package": "[fake] google-android-cmdline-tools-6.0-installer",
          "ludate": "2019-12-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.9.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.4.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-cmdline-tools-7.0-installer",
          "ludate": "2019-5-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 9.7.2",
          "fedora": "\u26a0\ufe0f 8.2.3",
          "openeuler": "\u2705 6.7.7",
          "ubuntu": "\u26a0\ufe0f 1.1.5",
          "package": "[fake] google-android-licenses",
          "ludate": "2019-12-4"
        },
        {
          "arch": "\u2705 9.3.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.2.2",
          "openeuler": "\u26a0\ufe0f 4.4.4",
          "ubuntu": "\u26a0\ufe0f 1.3.8",
          "package": "[fake] google-android-m2repository-installer",
          "ludate": "2019-1-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.1.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.5.9",
          "package": "[fake] google-android-patcher-4-installer",
          "ludate": "2019-1-11"
        },
        {
          "arch": "\u2705 7.9.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.6.3",
          "openeuler": "\u26a0\ufe0f 3.5.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-10-installer",
          "ludate": "2021-4-9"
        },
        {
          "arch": "\u2705 6.7.7",
          "debian": "\u26a0\ufe0f 7.6.6",
          "fedora": "\u2705 3.6.5",
          "openeuler": "\u2705 3.9.3",
          "ubuntu": "\u2705 6.7.2",
          "package": "[fake] google-android-platform-11-installer",
          "ludate": "2019-12-4"
        },
        {
          "arch": "\u2705 7.6.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.4.5",
          "ubuntu": "\u2705 9.3.8",
          "package": "[fake] google-android-platform-12-installer",
          "ludate": "2020-4-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 5.2.2",
          "fedora": "\u2705 2.9.9",
          "openeuler": "\u2705 6.7.7",
          "ubuntu": "\u2705 1.4.6",
          "package": "[fake] google-android-platform-13-installer",
          "ludate": "2019-1-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.9.7",
          "fedora": "\u26a0\ufe0f 9.8.3",
          "openeuler": "\u2705 7.8.1",
          "ubuntu": "\u26a0\ufe0f 9.1.1",
          "package": "[fake] google-android-platform-14-installer",
          "ludate": "2020-5-16"
        },
        {
          "arch": "\u2705 1.7.7",
          "debian": "\u2705 2.5.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-15-installer",
          "ludate": "2021-2-26"
        },
        {
          "arch": "\u2705 3.5.4",
          "debian": "\u2705 3.7.5",
          "fedora": "\u26a0\ufe0f 6.9.9",
          "openeuler": "\u2705 9.7.9",
          "ubuntu": "\u26a0\ufe0f 1.8.5",
          "package": "[fake] google-android-platform-16-installer",
          "ludate": "2021-11-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.9.1",
          "fedora": "\u2705 5.4.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.9.5",
          "package": "[fake] google-android-platform-17-installer",
          "ludate": "2021-2-7"
        },
        {
          "arch": "\u26a0\ufe0f 8.9.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.7.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-18-installer",
          "ludate": "2021-6-12"
        },
        {
          "arch": "\u2705 9.5.5",
          "debian": "\u26a0\ufe0f 2.3.2",
          "fedora": "\u2705 6.3.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.1.6",
          "package": "[fake] google-android-platform-19-installer",
          "ludate": "2021-9-6"
        },
        {
          "arch": "\u26a0\ufe0f 1.1.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.7.8",
          "openeuler": "\u26a0\ufe0f 4.3.4",
          "ubuntu": "\u26a0\ufe0f 7.1.4",
          "package": "[fake] google-android-platform-20-installer",
          "ludate": "2020-8-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 8.5.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.7.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-21-installer",
          "ludate": "2019-3-24"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 3.4.7",
          "fedora": "\u26a0\ufe0f 7.3.1",
          "openeuler": "\u2705 8.1.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-22-installer",
          "ludate": "2021-3-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.9.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.9.2",
          "package": "[fake] google-android-platform-23-installer",
          "ludate": "2019-5-28"
        },
        {
          "arch": "\u26a0\ufe0f 7.1.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.9.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 6.7.4",
          "package": "[fake] google-android-platform-24-installer",
          "ludate": "2019-4-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.9.4",
          "fedora": "\u26a0\ufe0f 1.8.5",
          "openeuler": "\u2705 9.9.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-25-installer",
          "ludate": "2021-10-8"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 8.4.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.8.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-26-installer",
          "ludate": "2019-9-28"
        },
        {
          "arch": "\u2705 6.5.4",
          "debian": "\u26a0\ufe0f 8.1.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 2.6.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-27-installer",
          "ludate": "2021-2-2"
        },
        {
          "arch": "\u2705 8.3.4",
          "debian": "\u2705 3.8.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 1.3.8",
          "ubuntu": "\u2705 9.8.9",
          "package": "[fake] google-android-platform-28-installer",
          "ludate": "2020-2-8"
        },
        {
          "arch": "\u26a0\ufe0f 1.1.9",
          "debian": "\u2705 3.7.8",
          "fedora": "\u2705 7.2.7",
          "openeuler": "\u26a0\ufe0f 6.6.7",
          "ubuntu": "\u2705 5.4.4",
          "package": "[fake] google-android-platform-29-installer",
          "ludate": "2020-12-25"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 3.6.3",
          "fedora": "\u2705 6.2.8",
          "openeuler": "\u26a0\ufe0f 9.3.5",
          "ubuntu": "\u2705 4.2.5",
          "package": "[fake] google-android-platform-30-installer",
          "ludate": "2019-7-25"
        },
        {
          "arch": "\u2705 1.8.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.6.4",
          "openeuler": "\u2705 9.5.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-31-installer",
          "ludate": "2019-1-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.5.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.3.9",
          "package": "[fake] google-android-platform-32-installer",
          "ludate": "2020-9-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.4.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.8.6",
          "package": "[fake] google-android-platform-33-installer",
          "ludate": "2021-6-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.8.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.3.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-platform-33-tiramisuprivacysandbox-installer",
          "ludate": "2020-5-11"
        },
        {
          "arch": "\u26a0\ufe0f 3.3.6",
          "debian": "\u26a0\ufe0f 6.8.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.8.3",
          "package": "[fake] google-android-platform-7-installer",
          "ludate": "2021-10-3"
        },
        {
          "arch": "\u26a0\ufe0f 6.2.5",
          "debian": "\u2705 9.7.4",
          "fedora": "\u2705 2.8.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.7.9",
          "package": "[fake] google-android-platform-8-installer",
          "ludate": "2019-3-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 2.3.1",
          "fedora": "\u26a0\ufe0f 1.8.1",
          "openeuler": "\u2705 1.5.6",
          "ubuntu": "\u2705 5.7.2",
          "package": "[fake] google-android-platform-9-installer",
          "ludate": "2021-10-8"
        },
        {
          "arch": "\u2705 7.5.4",
          "debian": "\u26a0\ufe0f 6.7.6",
          "fedora": "\u2705 6.3.5",
          "openeuler": "\u2705 3.2.7",
          "ubuntu": "\u26a0\ufe0f 6.7.2",
          "package": "[fake] google-android-sdk-docs-installer",
          "ludate": "2019-9-20"
        },
        {
          "arch": "\u26a0\ufe0f 4.2.2",
          "debian": "\u2705 3.5.1",
          "fedora": "\u2705 8.7.2",
          "openeuler": "\u26a0\ufe0f 1.6.1",
          "ubuntu": "\u2705 7.8.1",
          "package": "[fake] google-android-sources-15-installer",
          "ludate": "2020-1-27"
        },
        {
          "arch": "\u26a0\ufe0f 6.6.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.2.9",
          "openeuler": "\u26a0\ufe0f 6.9.2",
          "ubuntu": "\u26a0\ufe0f 4.5.5",
          "package": "[fake] google-android-sources-16-installer",
          "ludate": "2020-4-10"
        },
        {
          "arch": "\u2705 9.4.3",
          "debian": "\u26a0\ufe0f 6.3.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.7.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-sources-17-installer",
          "ludate": "2020-8-8"
        },
        {
          "arch": "\u2705 6.7.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 2.4.1",
          "openeuler": "\u26a0\ufe0f 3.1.5",
          "ubuntu": "\u26a0\ufe0f 4.4.4",
          "package": "[fake] google-android-sources-18-installer",
          "ludate": "2021-3-24"
        },
        {
          "arch": "\u26a0\ufe0f 3.1.1",
          "debian": "\u26a0\ufe0f 5.3.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.3.4",
          "ubuntu": "\u2705 2.8.9",
          "package": "[fake] google-android-sources-19-installer",
          "ludate": "2020-2-7"
        },
        {
          "arch": "\u2705 5.8.1",
          "debian": "\u26a0\ufe0f 3.7.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.5.4",
          "package": "[fake] google-android-sources-20-installer",
          "ludate": "2021-2-15"
        },
        {
          "arch": "\u2705 9.1.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.7.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.1.3",
          "package": "[fake] google-android-sources-21-installer",
          "ludate": "2021-6-5"
        },
        {
          "arch": "\u26a0\ufe0f 2.3.7",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 1.5.7",
          "ubuntu": "\u2705 2.7.9",
          "package": "[fake] google-android-sources-22-installer",
          "ludate": "2020-1-16"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.7",
          "debian": "\u26a0\ufe0f 5.3.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 2.8.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-sources-23-installer",
          "ludate": "2020-9-25"
        },
        {
          "arch": "\u2705 5.9.5",
          "debian": "\u2705 6.1.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.5.2",
          "ubuntu": "\u26a0\ufe0f 8.6.7",
          "package": "[fake] google-android-sources-24-installer",
          "ludate": "2019-2-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.3.3",
          "openeuler": "\u26a0\ufe0f 6.7.4",
          "ubuntu": "\u26a0\ufe0f 7.9.2",
          "package": "[fake] google-android-sources-25-installer",
          "ludate": "2019-6-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 8.5.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 9.3.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-sources-26-installer",
          "ludate": "2021-4-25"
        },
        {
          "arch": "\u2705 5.9.8",
          "debian": "\u2705 1.6.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.2.7",
          "package": "[fake] google-android-sources-27-installer",
          "ludate": "2020-1-18"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.6.7",
          "fedora": "\u26a0\ufe0f 7.4.2",
          "openeuler": "\u2705 4.7.3",
          "ubuntu": "\u26a0\ufe0f 4.8.7",
          "package": "[fake] google-android-sources-28-installer",
          "ludate": "2019-7-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.2.8",
          "fedora": "\u26a0\ufe0f 7.1.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.2.8",
          "package": "[fake] google-android-sources-29-installer",
          "ludate": "2021-8-25"
        },
        {
          "arch": "\u26a0\ufe0f 2.7.9",
          "debian": "\u2705 9.9.8",
          "fedora": "\u26a0\ufe0f 9.9.4",
          "openeuler": "\u26a0\ufe0f 9.3.6",
          "ubuntu": "\u2705 2.3.6",
          "package": "[fake] google-android-sources-30-installer",
          "ludate": "2020-2-14"
        },
        {
          "arch": "\u26a0\ufe0f 6.6.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 2.7.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] google-android-sources-31-installer",
          "ludate": "2019-7-18"
        },
        {
          "arch": "\u2705 4.5.2",
          "debian": "\u2705 8.9.6",
          "fedora": "\u26a0\ufe0f 2.8.5",
          "openeuler": "\u26a0\ufe0f 8.9.7",
          "ubuntu": "\u2705 5.2.4",
          "package": "[fake] google-android-sources-32-installer",
          "ludate": "2021-11-12"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.8.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gpustat",
          "ludate": "2020-7-7"
        },
        {
          "arch": "\u26a0\ufe0f 8.1.3",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.4.1",
          "package": "[fake] grr-client-templates",
          "ludate": "2021-10-4"
        },
        {
          "arch": "\u2705 4.8.2",
          "debian": "\u2705 2.1.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gsfonts-other",
          "ludate": "2020-10-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.4.2",
          "fedora": "\u2705 2.2.3",
          "openeuler": "\u26a0\ufe0f 4.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] gsl-doc-info",
          "ludate": "2020-11-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.1.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.5.8",
          "ubuntu": "\u2705 2.7.5",
          "package": "[fake] gsl-doc-pdf",
          "ludate": "2020-2-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.1.1",
          "fedora": "\u26a0\ufe0f 1.2.4",
          "openeuler": "\u26a0\ufe0f 4.4.4",
          "ubuntu": "\u2705 6.5.4",
          "package": "[fake] h264enc",
          "ludate": "2019-8-15"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.2.3",
          "fedora": "\u26a0\ufe0f 7.1.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.8.1",
          "package": "[fake] hashcat-nvidia",
          "ludate": "2020-6-16"
        },
        {
          "arch": "\u2705 7.3.8",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.2.5",
          "ubuntu": "\u26a0\ufe0f 5.3.3",
          "package": "[fake] hevea-doc",
          "ludate": "2019-9-18"
        },
        {
          "arch": "\u2705 9.3.1",
          "debian": "\u26a0\ufe0f 4.9.2",
          "fedora": "\u26a0\ufe0f 7.4.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] hijra-applet",
          "ludate": "2019-9-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 5.7.4",
          "openeuler": "\u2705 2.4.5",
          "ubuntu": "\u26a0\ufe0f 5.7.2",
          "package": "[fake] horae",
          "ludate": "2021-4-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.7.6",
          "openeuler": "\u2705 4.8.1",
          "ubuntu": "\u26a0\ufe0f 3.5.5",
          "package": "[fake] hts-voice-nitech-jp-atr503-m001",
          "ludate": "2019-5-16"
        },
        {
          "arch": "\u26a0\ufe0f 4.4.1",
          "debian": "\u2705 4.6.5",
          "fedora": "\u2705 4.1.7",
          "openeuler": "\u2705 2.1.4",
          "ubuntu": "\u26a0\ufe0f 5.5.4",
          "package": "[fake] hwb",
          "ludate": "2021-11-7"
        },
        {
          "arch": "\u2705 2.7.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 6.1.1",
          "openeuler": "\u2705 2.7.1",
          "ubuntu": "\u2705 9.2.5",
          "package": "[fake] hyperspec",
          "ludate": "2021-10-27"
        },
        {
          "arch": "\u2705 5.3.4",
          "debian": "\u2705 7.7.6",
          "fedora": "\u2705 3.5.6",
          "openeuler": "\u2705 8.8.9",
          "ubuntu": "\u2705 2.5.4",
          "package": "[fake] i965-va-driver-shaders",
          "ludate": "2021-11-21"
        },
        {
          "arch": "\u26a0\ufe0f 7.1.9",
          "debian": "\u26a0\ufe0f 4.4.2",
          "fedora": "\u2705 7.8.1",
          "openeuler": "\u26a0\ufe0f 4.4.6",
          "ubuntu": "\u26a0\ufe0f 3.3.7",
          "package": "[fake] icc-profiles",
          "ludate": "2019-8-15"
        },
        {
          "arch": "\u26a0\ufe0f 9.9.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.2.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.8.6",
          "package": "[fake] ifeffit-doc",
          "ludate": "2020-7-7"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.8.9",
          "fedora": "\u2705 2.9.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.6.8",
          "package": "[fake] inform-docs",
          "ludate": "2021-10-10"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.1",
          "debian": "\u2705 3.6.7",
          "fedora": "\u26a0\ufe0f 8.9.5",
          "openeuler": "\u2705 3.5.2",
          "ubuntu": "\u26a0\ufe0f 4.8.6",
          "package": "[fake] intel-media-va-driver-non-free",
          "ludate": "2020-5-23"
        },
        {
          "arch": "\u26a0\ufe0f 9.3.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.5.2",
          "openeuler": "\u2705 6.6.7",
          "ubuntu": "\u26a0\ufe0f 8.1.4",
          "package": "[fake] intel-mkl-doc",
          "ludate": "2020-9-20"
        },
        {
          "arch": "\u2705 4.6.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.9.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] jajuk",
          "ludate": "2019-11-8"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.6.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.9.7",
          "package": "[fake] java-package",
          "ludate": "2020-6-6"
        },
        {
          "arch": "\u26a0\ufe0f 4.1.7",
          "debian": "\u2705 9.6.7",
          "fedora": "\u26a0\ufe0f 1.7.9",
          "openeuler": "\u2705 7.5.8",
          "ubuntu": "\u26a0\ufe0f 3.9.3",
          "package": "[fake] jhove",
          "ludate": "2021-2-25"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.3.3",
          "fedora": "\u26a0\ufe0f 1.6.8",
          "openeuler": "\u2705 1.1.1",
          "ubuntu": "\u26a0\ufe0f 8.2.3",
          "package": "[fake] josm-installer",
          "ludate": "2020-8-20"
        },
        {
          "arch": "\u2705 2.4.3",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.8.6",
          "package": "[fake] kcemu-common",
          "ludate": "2019-11-1"
        },
        {
          "arch": "\u2705 8.2.1",
          "debian": "\u26a0\ufe0f 1.6.5",
          "fedora": "\u2705 2.8.4",
          "openeuler": "\u26a0\ufe0f 4.2.4",
          "ubuntu": "\u2705 2.9.5",
          "package": "[fake] kdeplasma-applets-xrdesktop",
          "ludate": "2020-7-20"
        },
        {
          "arch": "\u26a0\ufe0f 2.9.3",
          "debian": "\u26a0\ufe0f 3.3.8",
          "fedora": "\u2705 7.6.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 2.2.9",
          "package": "[fake] ldraw-parts",
          "ludate": "2020-4-13"
        },
        {
          "arch": "\u2705 1.8.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.8.4",
          "openeuler": "\u26a0\ufe0f 8.3.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libamgcl-dev",
          "ludate": "2020-2-11"
        },
        {
          "arch": "\u2705 9.3.8",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libcg",
          "ludate": "2019-3-25"
        },
        {
          "arch": "\u26a0\ufe0f 8.5.4",
          "debian": "\u26a0\ufe0f 2.1.8",
          "fedora": "\u2705 7.8.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libcggl",
          "ludate": "2019-9-17"
        },
        {
          "arch": "\u26a0\ufe0f 1.6.1",
          "debian": "\u2705 1.3.4",
          "fedora": "\u26a0\ufe0f 4.7.2",
          "openeuler": "\u26a0\ufe0f 4.7.9",
          "ubuntu": "\u26a0\ufe0f 6.2.5",
          "package": "[fake] libclamunrar",
          "ludate": "2021-7-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.1.2",
          "fedora": "\u2705 6.1.4",
          "openeuler": "\u26a0\ufe0f 5.9.1",
          "ubuntu": "\u2705 6.7.7",
          "package": "[fake] libcuda1-384",
          "ludate": "2020-10-8"
        },
        {
          "arch": "\u2705 4.6.8",
          "debian": "\u2705 4.6.6",
          "fedora": "\u2705 6.5.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libcupti-doc",
          "ludate": "2019-11-4"
        },
        {
          "arch": "\u26a0\ufe0f 9.4.9",
          "debian": "\u2705 7.9.4",
          "fedora": "\u2705 7.8.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.2.1",
          "package": "[fake] libdvd-pkg",
          "ludate": "2019-1-23"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.6.8",
          "ubuntu": "\u2705 4.9.8",
          "package": "[fake] libf2j-java",
          "ludate": "2019-2-25"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.5",
          "debian": "\u26a0\ufe0f 6.1.3",
          "fedora": "\u2705 4.8.7",
          "openeuler": "\u2705 5.5.1",
          "ubuntu": "\u26a0\ufe0f 4.7.1",
          "package": "[fake] libforms-doc",
          "ludate": "2020-5-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 4.7.5",
          "fedora": "\u26a0\ufe0f 3.6.5",
          "openeuler": "\u2705 7.8.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libjlapack-java",
          "ludate": "2019-6-20"
        },
        {
          "arch": "\u26a0\ufe0f 2.9.4",
          "debian": "\u2705 5.2.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.7.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libmagma-doc",
          "ludate": "2021-12-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.3.6",
          "openeuler": "\u26a0\ufe0f 5.8.1",
          "ubuntu": "\u26a0\ufe0f 9.5.3",
          "package": "[fake] libmtj-java",
          "ludate": "2020-6-2"
        },
        {
          "arch": "\u2705 8.7.8",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.3.2",
          "openeuler": "\u26a0\ufe0f 7.9.8",
          "ubuntu": "\u2705 8.2.7",
          "package": "[fake] libmtj-java-doc",
          "ludate": "2021-2-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.9.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.9.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libmyth-python",
          "ludate": "2019-6-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.7.5",
          "fedora": "\u2705 3.6.7",
          "openeuler": "\u2705 1.2.6",
          "ubuntu": "\u2705 7.4.7",
          "package": "[fake] libmythtv-perl",
          "ludate": "2021-2-21"
        },
        {
          "arch": "\u2705 2.6.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 2.6.2",
          "openeuler": "\u2705 7.9.8",
          "ubuntu": "\u2705 2.5.4",
          "package": "[fake] libnetlib-java",
          "ludate": "2021-11-28"
        },
        {
          "arch": "\u26a0\ufe0f 4.4.7",
          "debian": "\u2705 4.5.4",
          "fedora": "\u2705 5.2.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.7.2",
          "package": "[fake] libopenzwave-doc",
          "ludate": "2021-6-12"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 6.9.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 7.1.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] librem5-flash-image",
          "ludate": "2021-12-20"
        },
        {
          "arch": "\u26a0\ufe0f 6.8.7",
          "debian": "\u2705 3.7.8",
          "fedora": "\u2705 8.4.3",
          "openeuler": "\u2705 9.4.1",
          "ubuntu": "\u26a0\ufe0f 5.1.5",
          "package": "[fake] libstar-parser-perl",
          "ludate": "2019-11-25"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.9.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.5.8",
          "ubuntu": "\u2705 6.3.6",
          "package": "[fake] libtestu01-0-dev-common",
          "ludate": "2019-8-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.1.1",
          "openeuler": "\u2705 3.1.7",
          "ubuntu": "\u26a0\ufe0f 7.6.3",
          "package": "[fake] libthrust-dev",
          "ludate": "2020-7-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.3.9",
          "fedora": "\u26a0\ufe0f 1.2.7",
          "openeuler": "\u2705 5.6.7",
          "ubuntu": "\u26a0\ufe0f 9.5.6",
          "package": "[fake] libttspico-data",
          "ludate": "2019-11-4"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 2.1.7",
          "openeuler": "\u2705 2.4.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libttspico-dev",
          "ludate": "2021-11-25"
        },
        {
          "arch": "\u2705 1.4.5",
          "debian": "\u26a0\ufe0f 8.7.3",
          "fedora": "\u26a0\ufe0f 3.7.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.1.8",
          "package": "[fake] libttspico-utils",
          "ludate": "2019-11-3"
        },
        {
          "arch": "\u2705 8.9.8",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.7.1",
          "openeuler": "\u26a0\ufe0f 5.4.6",
          "ubuntu": "\u26a0\ufe0f 5.7.8",
          "package": "[fake] libttspico0",
          "ludate": "2021-11-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.9.4",
          "openeuler": "\u2705 5.5.3",
          "ubuntu": "\u2705 9.5.2",
          "package": "[fake] libunrar-headers",
          "ludate": "2019-12-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.3.9",
          "openeuler": "\u2705 7.8.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libvdjtools-java",
          "ludate": "2019-12-8"
        },
        {
          "arch": "\u2705 2.8.3",
          "debian": "\u2705 7.9.4",
          "fedora": "\u26a0\ufe0f 3.7.5",
          "openeuler": "\u2705 7.4.5",
          "ubuntu": "\u2705 1.9.6",
          "package": "[fake] libvideo-info-perl",
          "ludate": "2020-10-24"
        },
        {
          "arch": "\u26a0\ufe0f 1.5.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.6.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] libxml-compile-soap-perl",
          "ludate": "2021-4-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.1.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.1.1",
          "package": "[fake] libxml-compile-wsdl11-perl",
          "ludate": "2020-9-23"
        },
        {
          "arch": "\u26a0\ufe0f 2.6.5",
          "debian": "\u26a0\ufe0f 8.7.5",
          "fedora": "\u2705 9.2.6",
          "openeuler": "\u2705 6.7.9",
          "ubuntu": "\u2705 3.1.9",
          "package": "[fake] linux-firmware-xilinx-ap1302",
          "ludate": "2020-8-10"
        },
        {
          "arch": "\u2705 8.3.1",
          "debian": "\u26a0\ufe0f 3.1.1",
          "fedora": "\u26a0\ufe0f 4.9.7",
          "openeuler": "\u2705 8.3.4",
          "ubuntu": "\u2705 2.8.7",
          "package": "[fake] linux-firmware-xilinx-vcu",
          "ludate": "2019-8-23"
        },
        {
          "arch": "\u26a0\ufe0f 1.1.7",
          "debian": "\u26a0\ufe0f 1.4.5",
          "fedora": "\u2705 9.5.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] lmbench-doc",
          "ludate": "2021-12-15"
        },
        {
          "arch": "\u2705 6.3.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.7.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] lubuntu-restricted-extras",
          "ludate": "2021-7-15"
        },
        {
          "arch": "\u2705 9.1.4",
          "debian": "\u2705 6.4.5",
          "fedora": "\u2705 8.5.8",
          "openeuler": "\u2705 8.3.1",
          "ubuntu": "\u2705 6.3.2",
          "package": "[fake] lutris",
          "ludate": "2021-9-16"
        },
        {
          "arch": "\u2705 7.6.4",
          "debian": "\u26a0\ufe0f 8.3.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.7.4",
          "ubuntu": "\u2705 3.7.5",
          "package": "[fake] mame-extra",
          "ludate": "2019-9-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 7.8.1",
          "openeuler": "\u26a0\ufe0f 7.1.4",
          "ubuntu": "\u26a0\ufe0f 2.3.3",
          "package": "[fake] manpages-posix",
          "ludate": "2019-4-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.7.7",
          "openeuler": "\u26a0\ufe0f 5.4.9",
          "ubuntu": "\u2705 6.4.1",
          "package": "[fake] manpages-posix-dev",
          "ludate": "2019-10-11"
        },
        {
          "arch": "\u2705 9.3.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] maple-latex",
          "ludate": "2020-9-27"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 1.5.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mathjax-siunitx",
          "ludate": "2020-5-9"
        },
        {
          "arch": "\u2705 5.2.6",
          "debian": "\u26a0\ufe0f 7.2.9",
          "fedora": "\u26a0\ufe0f 1.1.1",
          "openeuler": "\u2705 4.9.7",
          "ubuntu": "\u2705 4.3.8",
          "package": "[fake] matlab-brain2mesh",
          "ludate": "2019-9-26"
        },
        {
          "arch": "\u26a0\ufe0f 7.6.6",
          "debian": "\u2705 5.7.5",
          "fedora": "\u26a0\ufe0f 4.6.8",
          "openeuler": "\u2705 2.8.4",
          "ubuntu": "\u26a0\ufe0f 4.1.4",
          "package": "[fake] matlab-gdf",
          "ludate": "2021-3-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.7.7",
          "ubuntu": "\u26a0\ufe0f 6.3.2",
          "package": "[fake] matlab-iso2mesh",
          "ludate": "2019-9-27"
        },
        {
          "arch": "\u26a0\ufe0f 4.7.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 7.4.4",
          "openeuler": "\u2705 7.3.3",
          "ubuntu": "\u26a0\ufe0f 7.5.5",
          "package": "[fake] matlab-jnifti",
          "ludate": "2020-11-16"
        },
        {
          "arch": "\u2705 7.6.8",
          "debian": "\u26a0\ufe0f 8.1.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.9.7",
          "package": "[fake] matlab-jsonlab",
          "ludate": "2020-2-28"
        },
        {
          "arch": "\u26a0\ufe0f 4.5.6",
          "debian": "\u2705 5.8.9",
          "fedora": "\u2705 1.6.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.5.3",
          "package": "[fake] matlab-support",
          "ludate": "2019-11-21"
        },
        {
          "arch": "\u2705 2.2.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 2.9.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] matlab-zmat",
          "ludate": "2021-11-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.7.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.3.3",
          "ubuntu": "\u2705 6.1.8",
          "package": "[fake] mbrola-af1",
          "ludate": "2020-3-27"
        },
        {
          "arch": "\u2705 1.5.1",
          "debian": "\u2705 7.5.5",
          "fedora": "\u2705 8.7.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-ar1",
          "ludate": "2020-8-4"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.3.5",
          "fedora": "\u26a0\ufe0f 8.4.7",
          "openeuler": "\u26a0\ufe0f 8.8.1",
          "ubuntu": "\u26a0\ufe0f 6.6.8",
          "package": "[fake] mbrola-ar2",
          "ludate": "2021-5-23"
        },
        {
          "arch": "\u2705 8.4.7",
          "debian": "\u2705 6.6.4",
          "fedora": "\u2705 9.2.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.5.5",
          "package": "[fake] mbrola-br1",
          "ludate": "2020-10-15"
        },
        {
          "arch": "\u26a0\ufe0f 5.2.5",
          "debian": "\u2705 4.4.5",
          "fedora": "\u2705 3.4.9",
          "openeuler": "\u26a0\ufe0f 3.3.4",
          "ubuntu": "\u2705 4.9.5",
          "package": "[fake] mbrola-br2",
          "ludate": "2021-9-3"
        },
        {
          "arch": "\u2705 9.2.8",
          "debian": "\u2705 1.8.9",
          "fedora": "\u26a0\ufe0f 3.6.9",
          "openeuler": "\u2705 6.1.8",
          "ubuntu": "\u26a0\ufe0f 3.9.6",
          "package": "[fake] mbrola-br3",
          "ludate": "2020-4-8"
        },
        {
          "arch": "\u26a0\ufe0f 1.8.5",
          "debian": "\u26a0\ufe0f 3.1.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 9.4.2",
          "package": "[fake] mbrola-br4",
          "ludate": "2020-11-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.7.4",
          "fedora": "\u26a0\ufe0f 4.2.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 9.2.5",
          "package": "[fake] mbrola-bz1",
          "ludate": "2019-11-25"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 9.6.7",
          "fedora": "\u26a0\ufe0f 4.9.6",
          "openeuler": "\u26a0\ufe0f 5.7.9",
          "ubuntu": "\u26a0\ufe0f 4.3.9",
          "package": "[fake] mbrola-ca1",
          "ludate": "2021-3-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.1.6",
          "openeuler": "\u26a0\ufe0f 9.3.7",
          "ubuntu": "\u26a0\ufe0f 4.8.1",
          "package": "[fake] mbrola-ca2",
          "ludate": "2019-10-10"
        },
        {
          "arch": "\u26a0\ufe0f 9.5.6",
          "debian": "\u26a0\ufe0f 7.7.3",
          "fedora": "\u26a0\ufe0f 1.9.3",
          "openeuler": "\u26a0\ufe0f 1.7.2",
          "ubuntu": "\u26a0\ufe0f 6.7.7",
          "package": "[fake] mbrola-cn1",
          "ludate": "2021-6-23"
        },
        {
          "arch": "\u26a0\ufe0f 8.8.2",
          "debian": "\u2705 5.7.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 1.3.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-cr1",
          "ludate": "2021-5-14"
        },
        {
          "arch": "\u2705 8.8.3",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.8.3",
          "package": "[fake] mbrola-cz1",
          "ludate": "2019-4-11"
        },
        {
          "arch": "\u26a0\ufe0f 5.8.3",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 2.4.9",
          "ubuntu": "\u26a0\ufe0f 2.1.1",
          "package": "[fake] mbrola-cz2",
          "ludate": "2020-4-3"
        },
        {
          "arch": "\u2705 3.1.4",
          "debian": "\u2705 6.7.2",
          "fedora": "\u2705 6.3.3",
          "openeuler": "\u26a0\ufe0f 7.4.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-de1",
          "ludate": "2019-3-18"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 4.9.6",
          "fedora": "\u26a0\ufe0f 1.8.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.9.2",
          "package": "[fake] mbrola-de2",
          "ludate": "2020-6-19"
        },
        {
          "arch": "\u26a0\ufe0f 8.7.9",
          "debian": "\u26a0\ufe0f 5.9.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 7.4.3",
          "ubuntu": "\u2705 7.1.4",
          "package": "[fake] mbrola-de3",
          "ludate": "2019-8-28"
        },
        {
          "arch": "\u26a0\ufe0f 6.9.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.2.1",
          "openeuler": "\u26a0\ufe0f 5.6.4",
          "ubuntu": "\u26a0\ufe0f 7.1.5",
          "package": "[fake] mbrola-de4",
          "ludate": "2021-6-27"
        },
        {
          "arch": "\u26a0\ufe0f 7.7.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.8.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 9.6.6",
          "package": "[fake] mbrola-de5",
          "ludate": "2021-12-1"
        },
        {
          "arch": "\u2705 3.6.9",
          "debian": "\u26a0\ufe0f 2.6.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.8.3",
          "ubuntu": "\u2705 3.6.6",
          "package": "[fake] mbrola-de6",
          "ludate": "2019-8-5"
        },
        {
          "arch": "\u2705 1.4.3",
          "debian": "\u26a0\ufe0f 7.5.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.5.6",
          "ubuntu": "\u26a0\ufe0f 6.3.4",
          "package": "[fake] mbrola-de7",
          "ludate": "2020-12-21"
        },
        {
          "arch": "\u2705 4.4.5",
          "debian": "\u2705 4.7.9",
          "fedora": "\u2705 3.2.7",
          "openeuler": "\u2705 9.9.1",
          "ubuntu": "\u2705 4.3.4",
          "package": "[fake] mbrola-de8",
          "ludate": "2020-10-1"
        },
        {
          "arch": "\u2705 1.3.6",
          "debian": "\u26a0\ufe0f 1.6.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.2.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-ee1",
          "ludate": "2020-7-27"
        },
        {
          "arch": "\u2705 6.5.2",
          "debian": "\u2705 4.2.9",
          "fedora": "\u26a0\ufe0f 4.9.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.8.1",
          "package": "[fake] mbrola-en1",
          "ludate": "2021-9-19"
        },
        {
          "arch": "\u26a0\ufe0f 2.6.1",
          "debian": "\u26a0\ufe0f 5.1.8",
          "fedora": "\u2705 9.2.1",
          "openeuler": "\u2705 3.8.4",
          "ubuntu": "\u2705 7.3.3",
          "package": "[fake] mbrola-es1",
          "ludate": "2021-1-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 7.5.7",
          "openeuler": "\u26a0\ufe0f 1.2.9",
          "ubuntu": "\u2705 5.4.1",
          "package": "[fake] mbrola-es2",
          "ludate": "2019-1-28"
        },
        {
          "arch": "\u26a0\ufe0f 3.8.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.1.6",
          "openeuler": "\u2705 9.5.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-es3",
          "ludate": "2021-2-22"
        },
        {
          "arch": "\u26a0\ufe0f 6.6.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.7.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.3.1",
          "package": "[fake] mbrola-es4",
          "ludate": "2020-8-24"
        },
        {
          "arch": "\u2705 3.2.3",
          "debian": "\u26a0\ufe0f 2.5.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 5.4.6",
          "ubuntu": "\u2705 9.7.4",
          "package": "[fake] mbrola-fr1",
          "ludate": "2021-11-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.2.8",
          "package": "[fake] mbrola-fr2",
          "ludate": "2019-11-19"
        },
        {
          "arch": "\u26a0\ufe0f 8.9.1",
          "debian": "\u2705 3.5.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.6.8",
          "ubuntu": "\u2705 5.4.8",
          "package": "[fake] mbrola-fr3",
          "ludate": "2020-10-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 1.5.6",
          "ubuntu": "\u2705 1.3.3",
          "package": "[fake] mbrola-fr4",
          "ludate": "2021-11-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.7.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.1.7",
          "package": "[fake] mbrola-fr5",
          "ludate": "2020-9-24"
        },
        {
          "arch": "\u26a0\ufe0f 2.5.2",
          "debian": "\u2705 6.1.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.9.9",
          "ubuntu": "\u26a0\ufe0f 1.4.4",
          "package": "[fake] mbrola-fr6",
          "ludate": "2019-6-14"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.4.5",
          "fedora": "\u2705 8.5.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 3.4.8",
          "package": "[fake] mbrola-fr7",
          "ludate": "2020-3-7"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 6.9.5",
          "fedora": "\u2705 4.8.9",
          "openeuler": "\u2705 1.3.4",
          "ubuntu": "\u26a0\ufe0f 8.5.4",
          "package": "[fake] mbrola-gr1",
          "ludate": "2021-9-4"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.2.2",
          "fedora": "\u2705 6.3.5",
          "openeuler": "\u2705 7.5.7",
          "ubuntu": "\u2705 5.5.5",
          "package": "[fake] mbrola-gr2",
          "ludate": "2020-1-9"
        },
        {
          "arch": "\u26a0\ufe0f 4.3.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.3.9",
          "openeuler": "\u26a0\ufe0f 3.4.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-hb1",
          "ludate": "2019-5-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.4.5",
          "package": "[fake] mbrola-hb2",
          "ludate": "2019-2-12"
        },
        {
          "arch": "\u2705 7.2.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.4.3",
          "openeuler": "\u26a0\ufe0f 9.5.7",
          "ubuntu": "\u2705 5.1.9",
          "package": "[fake] mbrola-hn1",
          "ludate": "2020-11-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.6.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.1.5",
          "package": "[fake] mbrola-hu1",
          "ludate": "2021-7-4"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.7.8",
          "openeuler": "\u2705 9.2.1",
          "ubuntu": "\u2705 3.6.7",
          "package": "[fake] mbrola-ic1",
          "ludate": "2019-1-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.8.5",
          "openeuler": "\u26a0\ufe0f 7.1.5",
          "ubuntu": "\u26a0\ufe0f 4.5.1",
          "package": "[fake] mbrola-id1",
          "ludate": "2019-9-5"
        },
        {
          "arch": "\u26a0\ufe0f 4.8.2",
          "debian": "\u26a0\ufe0f 3.5.7",
          "fedora": "\u26a0\ufe0f 3.9.9",
          "openeuler": "\u2705 3.5.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-in1",
          "ludate": "2021-2-24"
        },
        {
          "arch": "\u26a0\ufe0f 1.7.4",
          "debian": "\u26a0\ufe0f 5.7.1",
          "fedora": "\u2705 3.8.4",
          "openeuler": "\u26a0\ufe0f 9.3.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-in2",
          "ludate": "2019-3-17"
        },
        {
          "arch": "\u2705 8.3.8",
          "debian": "\u26a0\ufe0f 6.2.5",
          "fedora": "\u26a0\ufe0f 5.6.6",
          "openeuler": "\u26a0\ufe0f 6.6.8",
          "ubuntu": "\u2705 1.5.4",
          "package": "[fake] mbrola-ir1",
          "ludate": "2021-8-22"
        },
        {
          "arch": "\u2705 9.2.4",
          "debian": "\u26a0\ufe0f 5.2.4",
          "fedora": "\u26a0\ufe0f 9.2.7",
          "openeuler": "\u2705 9.3.4",
          "ubuntu": "\u26a0\ufe0f 9.6.9",
          "package": "[fake] mbrola-it1",
          "ludate": "2021-12-22"
        },
        {
          "arch": "\u26a0\ufe0f 1.4.4",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.2.3",
          "package": "[fake] mbrola-it2",
          "ludate": "2020-12-2"
        },
        {
          "arch": "\u2705 6.7.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.8.5",
          "openeuler": "\u2705 5.2.6",
          "ubuntu": "\u2705 9.5.7",
          "package": "[fake] mbrola-it3",
          "ludate": "2019-5-18"
        },
        {
          "arch": "\u26a0\ufe0f 7.1.8",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 1.8.4",
          "ubuntu": "\u2705 5.7.2",
          "package": "[fake] mbrola-it4",
          "ludate": "2020-7-25"
        },
        {
          "arch": "\u26a0\ufe0f 3.5.9",
          "debian": "\u2705 2.6.8",
          "fedora": "\u2705 5.4.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-jp1",
          "ludate": "2019-6-16"
        },
        {
          "arch": "\u2705 8.4.1",
          "debian": "\u2705 6.4.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 5.2.3",
          "ubuntu": "\u26a0\ufe0f 4.7.7",
          "package": "[fake] mbrola-jp2",
          "ludate": "2019-5-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.7.4",
          "fedora": "\u2705 7.2.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.4.4",
          "package": "[fake] mbrola-jp3",
          "ludate": "2020-9-15"
        },
        {
          "arch": "\u26a0\ufe0f 7.9.3",
          "debian": "\u26a0\ufe0f 8.2.1",
          "fedora": "\u26a0\ufe0f 4.3.2",
          "openeuler": "\u26a0\ufe0f 7.3.7",
          "ubuntu": "\u26a0\ufe0f 1.9.2",
          "package": "[fake] mbrola-la1",
          "ludate": "2021-5-1"
        },
        {
          "arch": "\u2705 2.9.1",
          "debian": "\u26a0\ufe0f 3.6.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 2.2.3",
          "package": "[fake] mbrola-lt1",
          "ludate": "2021-4-17"
        },
        {
          "arch": "\u26a0\ufe0f 2.5.5",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.4.7",
          "package": "[fake] mbrola-lt2",
          "ludate": "2021-7-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.4.3",
          "fedora": "\u2705 9.9.3",
          "openeuler": "\u26a0\ufe0f 2.4.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-ma1",
          "ludate": "2021-2-21"
        },
        {
          "arch": "\u2705 8.6.2",
          "debian": "\u26a0\ufe0f 1.8.9",
          "fedora": "\u2705 7.3.2",
          "openeuler": "\u2705 6.8.7",
          "ubuntu": "\u2705 3.1.1",
          "package": "[fake] mbrola-mx1",
          "ludate": "2020-11-22"
        },
        {
          "arch": "\u26a0\ufe0f 7.9.2",
          "debian": "\u2705 4.8.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 8.9.7",
          "package": "[fake] mbrola-mx2",
          "ludate": "2020-6-11"
        },
        {
          "arch": "\u2705 8.5.3",
          "debian": "\u26a0\ufe0f 5.2.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.6.5",
          "ubuntu": "\u26a0\ufe0f 8.7.8",
          "package": "[fake] mbrola-nl1",
          "ludate": "2021-7-24"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 2.6.4",
          "fedora": "\u2705 9.2.6",
          "openeuler": "\u26a0\ufe0f 5.9.3",
          "ubuntu": "\u2705 2.6.6",
          "package": "[fake] mbrola-nl2",
          "ludate": "2021-4-25"
        },
        {
          "arch": "\u2705 6.6.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.3.3",
          "openeuler": "\u26a0\ufe0f 3.9.6",
          "ubuntu": "\u2705 4.5.2",
          "package": "[fake] mbrola-nl3",
          "ludate": "2021-8-11"
        },
        {
          "arch": "\u26a0\ufe0f 4.7.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 1.9.3",
          "openeuler": "\u26a0\ufe0f 7.2.5",
          "ubuntu": "\u26a0\ufe0f 1.5.3",
          "package": "[fake] mbrola-nz1",
          "ludate": "2019-7-20"
        },
        {
          "arch": "\u26a0\ufe0f 9.7.6",
          "debian": "\u2705 6.2.2",
          "fedora": "\u2705 4.8.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-pl1",
          "ludate": "2020-5-17"
        },
        {
          "arch": "\u26a0\ufe0f 8.8.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.9.4",
          "openeuler": "\u2705 9.1.9",
          "ubuntu": "\u2705 5.5.6",
          "package": "[fake] mbrola-pt1",
          "ludate": "2020-8-27"
        },
        {
          "arch": "\u26a0\ufe0f 8.8.7",
          "debian": "\u2705 9.7.9",
          "fedora": "\u26a0\ufe0f 2.7.5",
          "openeuler": "\u26a0\ufe0f 8.6.3",
          "ubuntu": "\u26a0\ufe0f 9.8.7",
          "package": "[fake] mbrola-ro1",
          "ludate": "2020-6-11"
        },
        {
          "arch": "\u2705 3.4.5",
          "debian": "\u26a0\ufe0f 4.1.1",
          "fedora": "\u26a0\ufe0f 1.5.5",
          "openeuler": "\u2705 1.4.6",
          "ubuntu": "\u26a0\ufe0f 4.1.8",
          "package": "[fake] mbrola-sw1",
          "ludate": "2020-10-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 9.7.3",
          "fedora": "\u2705 8.6.7",
          "openeuler": "\u2705 3.3.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-sw2",
          "ludate": "2019-5-9"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.4.1",
          "openeuler": "\u2705 2.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-tl1",
          "ludate": "2019-11-13"
        },
        {
          "arch": "\u2705 5.6.1",
          "debian": "\u2705 6.9.7",
          "fedora": "\u26a0\ufe0f 8.1.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-tr1",
          "ludate": "2020-2-11"
        },
        {
          "arch": "\u2705 8.5.5",
          "debian": "\u26a0\ufe0f 2.7.3",
          "fedora": "\u2705 4.1.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-tr2",
          "ludate": "2019-1-15"
        },
        {
          "arch": "\u26a0\ufe0f 2.3.3",
          "debian": "\u2705 1.7.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.3.4",
          "package": "[fake] mbrola-us1",
          "ludate": "2020-7-19"
        },
        {
          "arch": "\u26a0\ufe0f 8.4.2",
          "debian": "\u2705 1.3.2",
          "fedora": "\u26a0\ufe0f 3.9.4",
          "openeuler": "\u2705 4.7.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mbrola-us2",
          "ludate": "2019-5-8"
        },
        {
          "arch": "\u2705 9.4.9",
          "debian": "\u26a0\ufe0f 9.7.3",
          "fedora": "\u26a0\ufe0f 5.3.5",
          "openeuler": "\u2705 9.8.9",
          "ubuntu": "\u2705 6.3.6",
          "package": "[fake] mbrola-us3",
          "ludate": "2019-5-12"
        },
        {
          "arch": "\u26a0\ufe0f 3.8.6",
          "debian": "\u26a0\ufe0f 5.4.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.7.2",
          "ubuntu": "\u2705 9.6.4",
          "package": "[fake] mbrola-vz1",
          "ludate": "2021-4-24"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 9.5.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.6.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mdk-doc",
          "ludate": "2019-9-23"
        },
        {
          "arch": "\u2705 2.4.4",
          "debian": "\u2705 4.9.2",
          "fedora": "\u26a0\ufe0f 7.6.2",
          "openeuler": "\u2705 9.3.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] midisport-firmware",
          "ludate": "2019-1-3"
        },
        {
          "arch": "\u26a0\ufe0f 7.1.7",
          "debian": "\u2705 2.5.9",
          "fedora": "\u2705 4.5.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.9.2",
          "package": "[fake] mpi-specs",
          "ludate": "2021-10-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.6.3",
          "fedora": "\u26a0\ufe0f 3.8.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mplayer-skins",
          "ludate": "2021-8-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.8.4",
          "fedora": "\u26a0\ufe0f 3.8.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.1.8",
          "package": "[fake] muttdown",
          "ludate": "2021-10-5"
        },
        {
          "arch": "\u2705 9.7.5",
          "debian": "\u2705 6.8.3",
          "fedora": "\u2705 6.1.7",
          "openeuler": "\u2705 3.4.6",
          "ubuntu": "\u2705 5.9.2",
          "package": "[fake] mythplugins",
          "ludate": "2021-9-20"
        },
        {
          "arch": "\u26a0\ufe0f 8.7.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.3.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.3.2",
          "package": "[fake] mythtv",
          "ludate": "2021-2-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.5.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 4.5.4",
          "ubuntu": "\u2705 5.3.9",
          "package": "[fake] mythtv-backend-master",
          "ludate": "2019-9-14"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.1.5",
          "openeuler": "\u2705 5.3.6",
          "ubuntu": "\u2705 9.3.6",
          "package": "[fake] mythtv-database",
          "ludate": "2019-11-11"
        },
        {
          "arch": "\u26a0\ufe0f 5.7.3",
          "debian": "\u26a0\ufe0f 7.9.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.7.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] mythtv-doc",
          "ludate": "2020-7-20"
        },
        {
          "arch": "\u26a0\ufe0f 6.2.3",
          "debian": "\u26a0\ufe0f 9.4.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.9.6",
          "ubuntu": "\u2705 3.4.5",
          "package": "[fake] mythtv-theme-mythbuntu",
          "ludate": "2019-5-13"
        },
        {
          "arch": "\u2705 7.6.2",
          "debian": "\u26a0\ufe0f 3.9.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 9.1.1",
          "ubuntu": "\u26a0\ufe0f 1.1.7",
          "package": "[fake] mythweb",
          "ludate": "2020-5-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.9.8",
          "fedora": "\u2705 9.2.2",
          "openeuler": "\u26a0\ufe0f 6.5.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] nikto",
          "ludate": "2020-1-24"
        },
        {
          "arch": "\u2705 7.8.6",
          "debian": "\u2705 9.6.3",
          "fedora": "\u26a0\ufe0f 4.3.8",
          "openeuler": "\u2705 7.8.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] notion-dev",
          "ludate": "2019-9-8"
        },
        {
          "arch": "\u26a0\ufe0f 4.5.1",
          "debian": "\u26a0\ufe0f 7.7.1",
          "fedora": "\u26a0\ufe0f 4.4.3",
          "openeuler": "\u26a0\ufe0f 1.4.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] nouveau-firmware",
          "ludate": "2021-1-24"
        },
        {
          "arch": "\u26a0\ufe0f 7.7.1",
          "debian": "\u2705 7.5.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 8.4.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] nvidia-cg-dev",
          "ludate": "2020-6-24"
        },
        {
          "arch": "\u2705 7.9.8",
          "debian": "\u26a0\ufe0f 5.8.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.1.7",
          "package": "[fake] nvidia-cg-doc",
          "ludate": "2020-8-9"
        },
        {
          "arch": "\u26a0\ufe0f 2.1.8",
          "debian": "\u2705 4.7.5",
          "fedora": "\u26a0\ufe0f 6.6.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.7.2",
          "package": "[fake] nvidia-cg-toolkit",
          "ludate": "2019-7-4"
        },
        {
          "arch": "\u2705 5.7.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.4.9",
          "ubuntu": "\u2705 2.9.9",
          "package": "[fake] nvidia-cuda-toolkit-doc",
          "ludate": "2021-3-13"
        },
        {
          "arch": "\u2705 5.8.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.8.5",
          "openeuler": "\u2705 3.1.6",
          "ubuntu": "\u26a0\ufe0f 9.1.6",
          "package": "[fake] nvidia-libopencl1-384",
          "ludate": "2021-11-8"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.4.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.4.5",
          "package": "[fake] nvidia-opencl-icd-384",
          "ludate": "2020-11-3"
        },
        {
          "arch": "\u2705 6.7.3",
          "debian": "\u26a0\ufe0f 2.2.2",
          "fedora": "\u2705 5.2.3",
          "openeuler": "\u26a0\ufe0f 9.4.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] nvpy",
          "ludate": "2021-3-23"
        },
        {
          "arch": "\u2705 8.2.2",
          "debian": "\u2705 7.4.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.7.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] ocaml-doc",
          "ludate": "2019-4-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.7.7",
          "fedora": "\u26a0\ufe0f 6.6.8",
          "openeuler": "\u2705 6.1.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] odpic-doc",
          "ludate": "2020-5-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 4.8.8",
          "fedora": "\u26a0\ufe0f 1.9.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.5.7",
          "package": "[fake] office2003-schemas",
          "ludate": "2020-7-19"
        },
        {
          "arch": "\u2705 3.5.2",
          "debian": "\u2705 3.4.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.7.6",
          "package": "[fake] ooohg",
          "ludate": "2021-6-15"
        },
        {
          "arch": "\u2705 8.1.5",
          "debian": "\u2705 7.9.7",
          "fedora": "\u2705 1.7.6",
          "openeuler": "\u26a0\ufe0f 3.4.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] openboard-fonts-nonfree",
          "ludate": "2019-2-4"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.4.9",
          "fedora": "\u2705 2.5.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.2.1",
          "package": "[fake] openmw-data",
          "ludate": "2020-12-2"
        },
        {
          "arch": "\u2705 5.2.2",
          "debian": "\u2705 9.4.2",
          "fedora": "\u2705 6.7.2",
          "openeuler": "\u26a0\ufe0f 3.4.3",
          "ubuntu": "\u26a0\ufe0f 6.3.5",
          "package": "[fake] openrct2-objects",
          "ludate": "2021-10-24"
        },
        {
          "arch": "\u2705 5.8.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 3.3.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] openrct2-title-sequences",
          "ludate": "2019-4-22"
        },
        {
          "arch": "\u2705 4.5.5",
          "debian": "\u26a0\ufe0f 3.5.5",
          "fedora": "\u26a0\ufe0f 1.9.6",
          "openeuler": "\u26a0\ufe0f 2.7.3",
          "ubuntu": "\u26a0\ufe0f 6.9.6",
          "package": "[fake] openttd-opensfx",
          "ludate": "2021-10-6"
        },
        {
          "arch": "\u2705 2.4.8",
          "debian": "\u2705 5.1.5",
          "fedora": "\u2705 4.8.7",
          "openeuler": "\u26a0\ufe0f 8.9.1",
          "ubuntu": "\u26a0\ufe0f 5.8.1",
          "package": "[fake] org-mode-doc",
          "ludate": "2021-8-20"
        },
        {
          "arch": "\u26a0\ufe0f 9.6.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.7.9",
          "ubuntu": "\u2705 6.7.6",
          "package": "[fake] os8",
          "ludate": "2020-11-17"
        },
        {
          "arch": "\u26a0\ufe0f 8.4.3",
          "debian": "\u26a0\ufe0f 5.1.9",
          "fedora": "\u26a0\ufe0f 1.6.6",
          "openeuler": "\u26a0\ufe0f 4.7.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] othman",
          "ludate": "2019-4-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.2.1",
          "fedora": "\u2705 2.6.7",
          "openeuler": "\u2705 6.4.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] out-of-order",
          "ludate": "2020-11-15"
        },
        {
          "arch": "\u2705 6.7.7",
          "debian": "\u2705 3.6.8",
          "fedora": "\u26a0\ufe0f 8.5.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 6.8.3",
          "package": "[fake] oysttyer",
          "ludate": "2020-3-10"
        },
        {
          "arch": "\u26a0\ufe0f 1.5.4",
          "debian": "\u2705 6.6.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.4.6",
          "ubuntu": "\u26a0\ufe0f 7.1.3",
          "package": "[fake] parmetis-doc",
          "ludate": "2020-2-3"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 8.1.3",
          "fedora": "\u26a0\ufe0f 2.7.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.3.3",
          "package": "[fake] php-mythtv",
          "ludate": "2021-6-18"
        },
        {
          "arch": "\u2705 4.5.3",
          "debian": "\u2705 9.7.5",
          "fedora": "\u2705 2.7.9",
          "openeuler": "\u2705 5.5.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] picon-domains",
          "ludate": "2019-2-19"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.8",
          "debian": "\u2705 6.7.5",
          "fedora": "\u2705 7.2.8",
          "openeuler": "\u26a0\ufe0f 7.4.7",
          "ubuntu": "\u26a0\ufe0f 4.1.1",
          "package": "[fake] picon-misc",
          "ludate": "2021-6-22"
        },
        {
          "arch": "\u26a0\ufe0f 1.2.4",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 5.8.8",
          "ubuntu": "\u26a0\ufe0f 7.2.6",
          "package": "[fake] picon-news",
          "ludate": "2020-5-9"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.4.8",
          "fedora": "\u26a0\ufe0f 1.9.7",
          "openeuler": "\u2705 7.9.2",
          "ubuntu": "\u2705 9.9.2",
          "package": "[fake] picon-unknown",
          "ludate": "2020-5-14"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.1.6",
          "openeuler": "\u26a0\ufe0f 8.2.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] picon-usenix",
          "ludate": "2019-10-23"
        },
        {
          "arch": "\u2705 2.2.6",
          "debian": "\u26a0\ufe0f 6.6.7",
          "fedora": "\u2705 3.9.5",
          "openeuler": "\u26a0\ufe0f 4.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] picon-users",
          "ludate": "2019-3-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.5.1",
          "fedora": "\u2705 5.6.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.6.2",
          "package": "[fake] picon-weather",
          "ludate": "2019-8-26"
        },
        {
          "arch": "\u2705 8.3.3",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 2.4.2",
          "openeuler": "\u26a0\ufe0f 5.3.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] play.it",
          "ludate": "2019-11-11"
        },
        {
          "arch": "\u26a0\ufe0f 5.1.3",
          "debian": "\u26a0\ufe0f 5.4.3",
          "fedora": "\u26a0\ufe0f 9.9.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] playonlinux",
          "ludate": "2021-5-20"
        },
        {
          "arch": "\u2705 4.3.5",
          "debian": "\u26a0\ufe0f 2.7.9",
          "fedora": "\u2705 1.9.9",
          "openeuler": "\u2705 9.9.1",
          "ubuntu": "\u2705 4.8.3",
          "package": "[fake] pokemmo-installer",
          "ludate": "2021-3-1"
        },
        {
          "arch": "\u26a0\ufe0f 3.4.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.8.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.3.8",
          "package": "[fake] pq",
          "ludate": "2021-9-22"
        },
        {
          "arch": "\u26a0\ufe0f 8.4.9",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 6.1.6",
          "ubuntu": "\u2705 8.6.5",
          "package": "[fake] primus-vk",
          "ludate": "2020-2-27"
        },
        {
          "arch": "\u26a0\ufe0f 4.3.8",
          "debian": "\u2705 9.8.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 1.1.9",
          "package": "[fake] proj-rdnap",
          "ludate": "2019-1-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.1.3",
          "fedora": "\u26a0\ufe0f 4.7.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.5.8",
          "package": "[fake] protontricks",
          "ludate": "2020-3-14"
        },
        {
          "arch": "\u2705 3.6.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.2.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.5.5",
          "package": "[fake] ptex-jtex",
          "ludate": "2019-2-18"
        },
        {
          "arch": "\u26a0\ufe0f 2.3.9",
          "debian": "\u2705 1.1.2",
          "fedora": "\u26a0\ufe0f 1.5.7",
          "openeuler": "\u26a0\ufe0f 4.3.3",
          "ubuntu": "\u26a0\ufe0f 7.5.5",
          "package": "[fake] publicfile-installer",
          "ludate": "2020-2-26"
        },
        {
          "arch": "\u26a0\ufe0f 3.5.1",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 3.1.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] pycsw",
          "ludate": "2020-6-2"
        },
        {
          "arch": "\u26a0\ufe0f 6.1.3",
          "debian": "\u26a0\ufe0f 6.9.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 6.6.3",
          "package": "[fake] pycsw-doc",
          "ludate": "2021-7-4"
        },
        {
          "arch": "\u26a0\ufe0f 3.4.8",
          "debian": "\u26a0\ufe0f 2.2.9",
          "fedora": "\u2705 7.5.7",
          "openeuler": "\u2705 6.2.1",
          "ubuntu": "\u26a0\ufe0f 4.7.4",
          "package": "[fake] pycsw-wsgi",
          "ludate": "2019-12-9"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.2.7",
          "fedora": "\u2705 1.7.6",
          "openeuler": "\u2705 8.4.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python-cx-oracle-doc",
          "ludate": "2020-6-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 9.6.3",
          "fedora": "\u26a0\ufe0f 3.1.1",
          "openeuler": "\u2705 8.9.3",
          "ubuntu": "\u26a0\ufe0f 6.6.4",
          "package": "[fake] python-drf-yasg-nonfree-doc",
          "ludate": "2021-8-2"
        },
        {
          "arch": "\u26a0\ufe0f 7.1.1",
          "debian": "\u2705 1.7.7",
          "fedora": "\u2705 7.7.5",
          "openeuler": "\u26a0\ufe0f 2.5.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python-pycuda-doc",
          "ludate": "2021-7-18"
        },
        {
          "arch": "\u26a0\ufe0f 5.5.2",
          "debian": "\u2705 1.1.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 1.5.3",
          "ubuntu": "\u2705 1.4.1",
          "package": "[fake] python-seqcluster-doc",
          "ludate": "2019-12-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.6.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 6.2.1",
          "ubuntu": "\u26a0\ufe0f 9.8.1",
          "package": "[fake] python3-chargebee",
          "ludate": "2019-9-21"
        },
        {
          "arch": "\u2705 2.2.2",
          "debian": "\u2705 8.3.2",
          "fedora": "\u26a0\ufe0f 6.2.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-chargebee2",
          "ludate": "2020-4-4"
        },
        {
          "arch": "\u2705 1.7.4",
          "debian": "\u26a0\ufe0f 2.8.5",
          "fedora": "\u2705 9.4.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-django-anymail",
          "ludate": "2021-9-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 4.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-doris",
          "ludate": "2021-1-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.8.7",
          "ubuntu": "\u26a0\ufe0f 9.8.3",
          "package": "[fake] python3-drf-yasg-nonfree",
          "ludate": "2021-5-18"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.8.5",
          "openeuler": "\u26a0\ufe0f 2.5.2",
          "ubuntu": "\u2705 2.6.8",
          "package": "[fake] python3-hijra",
          "ludate": "2021-10-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.3.3",
          "openeuler": "\u26a0\ufe0f 6.4.1",
          "ubuntu": "\u26a0\ufe0f 4.6.9",
          "package": "[fake] python3-okasha",
          "ludate": "2019-8-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.2.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 2.3.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-okasha-examples",
          "ludate": "2021-10-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 9.2.4",
          "openeuler": "\u2705 4.7.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-othman",
          "ludate": "2019-12-24"
        },
        {
          "arch": "\u2705 5.9.6",
          "debian": "\u2705 3.8.2",
          "fedora": "\u26a0\ufe0f 5.9.6",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] python3-pycsw",
          "ludate": "2019-4-18"
        },
        {
          "arch": "\u2705 4.4.5",
          "debian": "\u26a0\ufe0f 1.7.1",
          "fedora": "\u2705 2.5.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.5.4",
          "package": "[fake] python3-pynliner",
          "ludate": "2021-4-24"
        },
        {
          "arch": "\u26a0\ufe0f 4.6.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 6.1.2",
          "openeuler": "\u2705 2.4.5",
          "ubuntu": "\u26a0\ufe0f 6.4.1",
          "package": "[fake] python3-seqcluster",
          "ludate": "2019-9-4"
        },
        {
          "arch": "\u2705 6.3.1",
          "debian": "\u2705 9.9.8",
          "fedora": "\u26a0\ufe0f 9.8.2",
          "openeuler": "\u2705 1.5.9",
          "ubuntu": "\u2705 2.3.6",
          "package": "[fake] python3-sparkpost",
          "ludate": "2021-4-26"
        },
        {
          "arch": "\u2705 3.3.6",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 9.5.7",
          "ubuntu": "\u26a0\ufe0f 9.5.9",
          "package": "[fake] python3-vertica",
          "ludate": "2020-2-20"
        },
        {
          "arch": "\u26a0\ufe0f 7.8.4",
          "debian": "\u26a0\ufe0f 2.6.1",
          "fedora": "\u2705 8.9.5",
          "openeuler": "\u26a0\ufe0f 9.7.5",
          "ubuntu": "\u26a0\ufe0f 2.7.5",
          "package": "[fake] quake",
          "ludate": "2021-1-11"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.8.9",
          "openeuler": "\u26a0\ufe0f 6.1.3",
          "ubuntu": "\u26a0\ufe0f 5.4.1",
          "package": "[fake] quake-server",
          "ludate": "2020-1-21"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 3.2.3",
          "fedora": "\u26a0\ufe0f 7.1.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.8.3",
          "package": "[fake] quake2",
          "ludate": "2021-8-13"
        },
        {
          "arch": "\u26a0\ufe0f 9.3.6",
          "debian": "\u26a0\ufe0f 4.3.2",
          "fedora": "\u2705 2.5.4",
          "openeuler": "\u26a0\ufe0f 2.5.6",
          "ubuntu": "\u26a0\ufe0f 6.3.6",
          "package": "[fake] quake2-server",
          "ludate": "2020-6-8"
        },
        {
          "arch": "\u26a0\ufe0f 3.5.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 4.2.8",
          "openeuler": "\u2705 6.1.5",
          "ubuntu": "\u2705 7.4.1",
          "package": "[fake] quake3",
          "ludate": "2019-6-28"
        },
        {
          "arch": "\u2705 9.7.7",
          "debian": "\u26a0\ufe0f 3.2.5",
          "fedora": "\u26a0\ufe0f 8.3.8",
          "openeuler": "\u26a0\ufe0f 8.5.3",
          "ubuntu": "\u26a0\ufe0f 7.6.5",
          "package": "[fake] quake3-data",
          "ludate": "2021-1-16"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 7.8.2",
          "fedora": "\u26a0\ufe0f 3.9.2",
          "openeuler": "\u2705 1.4.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] quake3-server",
          "ludate": "2021-8-20"
        },
        {
          "arch": "\u2705 1.7.2",
          "debian": "\u26a0\ufe0f 7.5.6",
          "fedora": "\u26a0\ufe0f 8.6.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] quake4",
          "ludate": "2019-12-2"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.2.8",
          "package": "[fake] quake4-server",
          "ludate": "2019-12-20"
        },
        {
          "arch": "\u2705 6.5.9",
          "debian": "\u26a0\ufe0f 3.8.4",
          "fedora": "\u2705 7.4.1",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 3.9.9",
          "package": "[fake] r4d",
          "ludate": "2021-4-25"
        },
        {
          "arch": "\u2705 7.3.9",
          "debian": "\u2705 3.2.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.1.1",
          "ubuntu": "\u26a0\ufe0f 8.3.7",
          "package": "[fake] r8125-dkms",
          "ludate": "2020-12-5"
        },
        {
          "arch": "\u2705 2.1.7",
          "debian": "\u2705 2.9.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.9.4",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] raster3d-doc",
          "ludate": "2019-9-14"
        },
        {
          "arch": "\u2705 3.7.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.7.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.1.6",
          "package": "[fake] repo",
          "ludate": "2019-2-9"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 1.9.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 9.9.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] revolution-r",
          "ludate": "2020-10-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.7.8",
          "fedora": "\u2705 1.6.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.3.3",
          "package": "[fake] rhvoice-albanian",
          "ludate": "2021-8-26"
        },
        {
          "arch": "\u2705 3.4.2",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.5.1",
          "ubuntu": "\u26a0\ufe0f 1.9.8",
          "package": "[fake] rhvoice-brazilian-portuguese",
          "ludate": "2021-8-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 1.1.3",
          "fedora": "\u2705 2.5.4",
          "openeuler": "\u26a0\ufe0f 7.4.1",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] rhvoice-english",
          "ludate": "2021-7-23"
        },
        {
          "arch": "\u26a0\ufe0f 6.3.6",
          "debian": "\u26a0\ufe0f 2.6.8",
          "fedora": "\u2705 2.4.5",
          "openeuler": "\u26a0\ufe0f 8.5.5",
          "ubuntu": "\u2705 2.7.1",
          "package": "[fake] rhvoice-esperanto",
          "ludate": "2020-5-24"
        },
        {
          "arch": "\u26a0\ufe0f 9.7.9",
          "debian": "\u26a0\ufe0f 7.6.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 3.5.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] rhvoice-kyrgyz",
          "ludate": "2021-1-25"
        },
        {
          "arch": "\u26a0\ufe0f 2.9.8",
          "debian": "\u2705 1.1.4",
          "fedora": "\u2705 1.9.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] rhvoice-macedonian",
          "ludate": "2021-7-14"
        },
        {
          "arch": "\u2705 5.2.1",
          "debian": "\u2705 1.1.2",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 6.2.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] rhvoice-polish",
          "ludate": "2019-7-6"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.4.3",
          "fedora": "\u2705 4.9.4",
          "openeuler": "\u26a0\ufe0f 7.8.9",
          "ubuntu": "\u2705 4.8.8",
          "package": "[fake] rhvoice-russian",
          "ludate": "2019-3-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.7.1",
          "package": "[fake] rhvoice-tatar",
          "ludate": "2021-2-13"
        },
        {
          "arch": "\u2705 4.6.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.6.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 5.5.1",
          "package": "[fake] rhvoice-ukrainian",
          "ludate": "2019-5-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 6.1.3",
          "openeuler": "\u2705 2.6.7",
          "ubuntu": "\u2705 6.6.2",
          "package": "[fake] ruby-googlecharts",
          "ludate": "2019-6-7"
        },
        {
          "arch": "\u2705 7.4.1",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.5.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 4.5.9",
          "package": "[fake] ruby-graphiql-rails",
          "ludate": "2019-8-21"
        },
        {
          "arch": "\u2705 2.1.3",
          "debian": "\u26a0\ufe0f 1.1.4",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.1.8",
          "ubuntu": "\u26a0\ufe0f 4.2.6",
          "package": "[fake] ruby-spamcheck",
          "ludate": "2021-6-23"
        },
        {
          "arch": "\u2705 4.9.7",
          "debian": "\u26a0\ufe0f 7.5.4",
          "fedora": "\u2705 9.8.3",
          "openeuler": "\u26a0\ufe0f 9.1.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] ruby-view-component",
          "ludate": "2020-5-11"
        },
        {
          "arch": "\u26a0\ufe0f 3.4.7",
          "debian": "\u2705 7.4.1",
          "fedora": "\u2705 3.9.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 1.5.9",
          "package": "[fake] runescape",
          "ludate": "2020-12-19"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.7.5",
          "fedora": "\u26a0\ufe0f 5.8.2",
          "openeuler": "\u2705 1.2.5",
          "ubuntu": "\u26a0\ufe0f 9.7.4",
          "package": "[fake] sabnzbdplus",
          "ludate": "2020-4-22"
        },
        {
          "arch": "\u26a0\ufe0f 1.6.4",
          "debian": "\u26a0\ufe0f 8.3.4",
          "fedora": "\u26a0\ufe0f 3.5.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] sauerbraten",
          "ludate": "2019-12-16"
        },
        {
          "arch": "\u26a0\ufe0f 5.9.3",
          "debian": "\u26a0\ufe0f 9.1.8",
          "fedora": "\u2705 2.4.9",
          "openeuler": "\u2705 4.6.4",
          "ubuntu": "\u2705 7.1.3",
          "package": "[fake] sauerbraten-server",
          "ludate": "2019-12-20"
        },
        {
          "arch": "\u26a0\ufe0f 9.3.9",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.3.1",
          "package": "[fake] scribus-doc",
          "ludate": "2019-7-20"
        },
        {
          "arch": "\u2705 7.2.9",
          "debian": "\u26a0\ufe0f 3.8.3",
          "fedora": "\u26a0\ufe0f 2.6.5",
          "openeuler": "\u2705 4.1.7",
          "ubuntu": "\u2705 4.8.1",
          "package": "[fake] selfhtml",
          "ludate": "2021-11-14"
        },
        {
          "arch": "\u26a0\ufe0f 6.9.7",
          "debian": "\u26a0\ufe0f 8.4.9",
          "fedora": "\u26a0\ufe0f 5.4.8",
          "openeuler": "\u26a0\ufe0f 5.9.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] seqcluster",
          "ludate": "2021-2-26"
        },
        {
          "arch": "\u2705 5.3.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 5.1.3",
          "openeuler": "\u26a0\ufe0f 9.2.9",
          "ubuntu": "\u26a0\ufe0f 9.1.3",
          "package": "[fake] sfcb-test",
          "ludate": "2020-2-20"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 5.2.8",
          "openeuler": "\u26a0\ufe0f 8.7.5",
          "ubuntu": "\u26a0\ufe0f 1.1.1",
          "package": "[fake] sgb-doc",
          "ludate": "2020-10-3"
        },
        {
          "arch": "\u26a0\ufe0f 5.1.6",
          "debian": "\u2705 5.1.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.8.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] shapetools-tutorial",
          "ludate": "2021-5-26"
        },
        {
          "arch": "\u26a0\ufe0f 2.8.7",
          "debian": "\u26a0\ufe0f 3.2.2",
          "fedora": "\u26a0\ufe0f 7.8.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] sisu-markup-samples",
          "ludate": "2019-11-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.1.6",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.7.1",
          "package": "[fake] sl-modem-dkms",
          "ludate": "2020-9-7"
        },
        {
          "arch": "\u26a0\ufe0f 9.5.9",
          "debian": "\u26a0\ufe0f 2.1.5",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 8.7.6",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] snmp-mibs-downloader",
          "ludate": "2021-10-5"
        },
        {
          "arch": "\u2705 1.2.6",
          "debian": "\u26a0\ufe0f 8.2.8",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.6.2",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] solvate-doc",
          "ludate": "2021-8-22"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 9.5.5",
          "openeuler": "\u2705 8.5.3",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] spectrum-roms",
          "ludate": "2020-4-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.6.1",
          "fedora": "\u26a0\ufe0f 4.5.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] speech-dispatcher-ibmtts",
          "ludate": "2021-6-27"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 1.3.5",
          "openeuler": "\u2705 4.2.4",
          "ubuntu": "\u2705 3.5.9",
          "package": "[fake] speech-dispatcher-ivona",
          "ludate": "2021-4-10"
        },
        {
          "arch": "\u2705 5.8.6",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.3.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] speech-dispatcher-pico",
          "ludate": "2020-11-28"
        },
        {
          "arch": "\u26a0\ufe0f 6.6.6",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 1.7.8",
          "ubuntu": "\u26a0\ufe0f 4.7.8",
          "package": "[fake] speech-dispatcher-voxin",
          "ludate": "2019-5-12"
        },
        {
          "arch": "\u26a0\ufe0f 2.8.3",
          "debian": "\u2705 7.3.7",
          "fedora": "\u26a0\ufe0f 5.9.1",
          "openeuler": "\u2705 7.3.4",
          "ubuntu": "\u26a0\ufe0f 3.6.8",
          "package": "[fake] spellcast-doc",
          "ludate": "2021-4-17"
        },
        {
          "arch": "\u26a0\ufe0f 8.1.9",
          "debian": "\u26a0\ufe0f 9.5.8",
          "fedora": "\u26a0\ufe0f 1.3.9",
          "openeuler": "\u2705 6.6.2",
          "ubuntu": "\u26a0\ufe0f 9.3.2",
          "package": "[fake] spread-phy",
          "ludate": "2020-12-12"
        },
        {
          "arch": "\u26a0\ufe0f 2.5.9",
          "debian": "\u26a0\ufe0f 8.4.8",
          "fedora": "\u2705 4.1.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.5.6",
          "package": "[fake] sqlcl-package",
          "ludate": "2020-9-11"
        },
        {
          "arch": "\u2705 5.9.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 7.5.6",
          "openeuler": "\u26a0\ufe0f 2.1.2",
          "ubuntu": "\u2705 1.3.1",
          "package": "[fake] sqldeveloper-package",
          "ludate": "2021-2-17"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 8.9.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.9.2",
          "package": "[fake] stardict-english-czech",
          "ludate": "2020-2-9"
        },
        {
          "arch": "\u2705 7.8.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 5.6.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] stardict-german-czech",
          "ludate": "2019-7-9"
        },
        {
          "arch": "\u2705 7.1.2",
          "debian": "\u26a0\ufe0f 1.5.9",
          "fedora": "\u26a0\ufe0f 1.8.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 2.5.3",
          "package": "[fake] steam",
          "ludate": "2021-1-4"
        },
        {
          "arch": "\u26a0\ufe0f 2.6.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 4.6.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] steam-devices",
          "ludate": "2021-10-21"
        },
        {
          "arch": "\u2705 1.6.7",
          "debian": "\u2705 8.5.9",
          "fedora": "\u26a0\ufe0f 8.7.6",
          "openeuler": "\u2705 9.8.5",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] steam-installer",
          "ludate": "2020-3-28"
        },
        {
          "arch": "\u26a0\ufe0f 4.9.6",
          "debian": "\u2705 8.4.2",
          "fedora": "\u26a0\ufe0f 7.1.6",
          "openeuler": "\u26a0\ufe0f 1.1.7",
          "ubuntu": "\u26a0\ufe0f 5.8.6",
          "package": "[fake] steamcmd",
          "ludate": "2021-12-21"
        },
        {
          "arch": "\u2705 7.5.7",
          "debian": "\u2705 6.5.4",
          "fedora": "\u2705 6.7.8",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] sugar-etoys-activity",
          "ludate": "2019-3-11"
        },
        {
          "arch": "\u26a0\ufe0f 1.1.1",
          "debian": "\u26a0\ufe0f 4.3.7",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 2.7.7",
          "ubuntu": "\u26a0\ufe0f 2.7.6",
          "package": "[fake] susv2",
          "ludate": "2020-8-1"
        },
        {
          "arch": "\u2705 2.7.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.8.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 4.1.5",
          "package": "[fake] susv3",
          "ludate": "2021-6-8"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 3.2.8",
          "ubuntu": "\u2705 5.2.2",
          "package": "[fake] susv4",
          "ludate": "2019-10-13"
        },
        {
          "arch": "\u26a0\ufe0f 8.3.9",
          "debian": "\u2705 5.1.2",
          "fedora": "\u2705 5.8.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] svtools",
          "ludate": "2021-4-28"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.1.2",
          "fedora": "\u26a0\ufe0f 5.3.3",
          "openeuler": "\u2705 4.9.4",
          "ubuntu": "\u26a0\ufe0f 3.1.4",
          "package": "[fake] t1-xfree86-nonfree",
          "ludate": "2021-11-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.1.2",
          "fedora": "\u26a0\ufe0f 2.3.5",
          "openeuler": "\u26a0\ufe0f 6.2.6",
          "ubuntu": "\u2705 9.2.1",
          "package": "[fake] testu01-data",
          "ludate": "2019-1-11"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 5.5.2",
          "fedora": "\u26a0\ufe0f 6.9.9",
          "openeuler": "\u2705 4.3.7",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] testu01-doc",
          "ludate": "2021-1-21"
        },
        {
          "arch": "\u26a0\ufe0f 6.7.7",
          "debian": "\u2705 5.4.9",
          "fedora": "\u2705 1.7.4",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 8.4.8",
          "package": "[fake] thawab",
          "ludate": "2019-2-16"
        },
        {
          "arch": "\u26a0\ufe0f 9.7.3",
          "debian": "\u26a0\ufe0f 1.4.9",
          "fedora": "\u2705 3.9.6",
          "openeuler": "\u2705 6.9.7",
          "ubuntu": "\u26a0\ufe0f 8.4.3",
          "package": "[fake] tightvnc-java",
          "ludate": "2020-10-28"
        },
        {
          "arch": "\u2705 2.4.2",
          "debian": "\u26a0\ufe0f 3.4.9",
          "fedora": "\u2705 3.4.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 2.2.6",
          "package": "[fake] translate-shell",
          "ludate": "2021-3-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 5.2.2",
          "fedora": "\u2705 2.9.1",
          "openeuler": "\u26a0\ufe0f 1.4.2",
          "ubuntu": "\u26a0\ufe0f 3.7.6",
          "package": "[fake] treeview",
          "ludate": "2020-4-15"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 7.4.4",
          "package": "[fake] trnascan-se-common",
          "ludate": "2019-9-13"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 4.7.3",
          "fedora": "\u26a0\ufe0f 6.4.7",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 9.6.6",
          "package": "[fake] ttf-mscorefonts-installer",
          "ludate": "2020-5-13"
        },
        {
          "arch": "\u26a0\ufe0f 4.2.6",
          "debian": "\u2705 9.8.6",
          "fedora": "\u2705 6.4.9",
          "openeuler": "\u2705 3.8.7",
          "ubuntu": "\u2705 5.6.4",
          "package": "[fake] ttf-xfree86-nonfree",
          "ludate": "2019-5-10"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 3.5.1",
          "fedora": "\u2705 3.2.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.1.6",
          "package": "[fake] ttf-xfree86-nonfree-syriac",
          "ludate": "2020-7-14"
        },
        {
          "arch": "\u2705 9.7.9",
          "debian": "\u2705 6.4.1",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 5.6.9",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] ugene-data",
          "ludate": "2020-10-8"
        },
        {
          "arch": "\u26a0\ufe0f 3.7.2",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.7.3",
          "openeuler": "\u26a0\ufe0f 2.3.7",
          "ubuntu": "\u26a0\ufe0f 4.3.2",
          "package": "[fake] uhexen2-common",
          "ludate": "2019-6-7"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 8.5.5",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.7.6",
          "package": "[fake] uqm-content",
          "ludate": "2019-11-23"
        },
        {
          "arch": "\u2705 9.8.1",
          "debian": "\u2705 9.7.5",
          "fedora": "\u2705 4.7.9",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u26a0\ufe0f 5.7.4",
          "package": "[fake] uqm-music",
          "ludate": "2021-6-24"
        },
        {
          "arch": "\u2705 8.5.4",
          "debian": "\u2705 8.5.7",
          "fedora": "\u2705 1.6.7",
          "openeuler": "\u26a0\ufe0f 3.9.3",
          "ubuntu": "\u2705 9.5.3",
          "package": "[fake] uqm-russian",
          "ludate": "2019-12-21"
        },
        {
          "arch": "\u2705 5.8.5",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.6.2",
          "openeuler": "\u2705 8.9.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] uqm-voice",
          "ludate": "2019-10-11"
        },
        {
          "arch": "\u2705 4.8.4",
          "debian": "\u2705 6.2.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u2705 7.8.8",
          "ubuntu": "\u2705 5.4.4",
          "package": "[fake] vdjtools",
          "ludate": "2020-12-5"
        },
        {
          "arch": "\u2705 3.9.8",
          "debian": "\u2705 4.1.7",
          "fedora": "\u2705 9.5.2",
          "openeuler": "\u26a0\ufe0f 8.5.7",
          "ubuntu": "\u2705 8.2.2",
          "package": "[fake] virtualbox-ext-pack",
          "ludate": "2020-2-17"
        },
        {
          "arch": "\u2705 8.6.9",
          "debian": "\u26a0\ufe0f 9.2.1",
          "fedora": "\u2705 7.7.2",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] virtualbox-guest-additions-iso",
          "ludate": "2019-8-23"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 5.6.3",
          "fedora": "\u2705 5.2.2",
          "openeuler": "\u2705 5.1.3",
          "ubuntu": "\u26a0\ufe0f 1.7.7",
          "package": "[fake] vmware-manager",
          "ludate": "2020-2-24"
        },
        {
          "arch": "\u26a0\ufe0f 9.5.4",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 6.4.7",
          "openeuler": "\u26a0\ufe0f 9.2.7",
          "ubuntu": "\u26a0\ufe0f 6.9.9",
          "package": "[fake] weirdx",
          "ludate": "2019-6-19"
        },
        {
          "arch": "\u26a0\ufe0f 4.3.2",
          "debian": "\u2705 9.3.3",
          "fedora": "\ud83d\udeab",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] wnn7egg",
          "ludate": "2019-8-5"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 9.8.2",
          "fedora": "\u26a0\ufe0f 3.7.3",
          "openeuler": "\u26a0\ufe0f 9.4.5",
          "ubuntu": "\u26a0\ufe0f 6.1.7",
          "package": "[fake] xfonts-naga10",
          "ludate": "2021-6-1"
        },
        {
          "arch": "\u26a0\ufe0f 7.4.7",
          "debian": "\ud83d\udeab",
          "fedora": "\u26a0\ufe0f 8.1.6",
          "openeuler": "\u26a0\ufe0f 9.8.9",
          "ubuntu": "\u26a0\ufe0f 1.7.1",
          "package": "[fake] xml2rfc",
          "ludate": "2020-1-26"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u26a0\ufe0f 6.6.1",
          "fedora": "\u26a0\ufe0f 6.7.8",
          "openeuler": "\u26a0\ufe0f 3.4.8",
          "ubuntu": "\u26a0\ufe0f 7.2.7",
          "package": "[fake] xtide-data-nonfree",
          "ludate": "2019-8-12"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 2.1.2",
          "fedora": "\u26a0\ufe0f 4.6.1",
          "openeuler": "\u26a0\ufe0f 7.6.5",
          "ubuntu": "\u2705 9.6.5",
          "package": "[fake] xubuntu-restricted-addons",
          "ludate": "2020-6-18"
        },
        {
          "arch": "\u26a0\ufe0f 4.6.1",
          "debian": "\u2705 4.7.9",
          "fedora": "\ud83d\udeab",
          "openeuler": "\u26a0\ufe0f 7.6.8",
          "ubuntu": "\ud83d\udeab",
          "package": "[fake] xvidenc",
          "ludate": "2019-11-12"
        },
        {
          "arch": "\u26a0\ufe0f 9.8.5",
          "debian": "\u2705 4.3.7",
          "fedora": "\u2705 9.3.8",
          "openeuler": "\u2705 3.1.9",
          "ubuntu": "\u2705 7.2.4",
          "package": "[fake] yale",
          "ludate": "2021-9-1"
        },
        {
          "arch": "\ud83d\udeab",
          "debian": "\u2705 7.7.6",
          "fedora": "\u2705 2.3.3",
          "openeuler": "\ud83d\udeab",
          "ubuntu": "\u2705 7.6.1",
          "package": "[fake] zangband-data",
          "ludate": "2020-8-28"
        },
        {
          "arch": "\u2705 9.2.9",
          "debian": "\ud83d\udeab",
          "fedora": "\u2705 3.9.4",
          "openeuler": "\u2705 8.3.7",
          "ubuntu": "\u26a0\ufe0f 8.5.7",
          "package": "[fake] zeroc-ice-manual",
          "ludate": "2020-12-23"
        }
      ]
    }
  },
  methods: {
    handle(url) {
      window.location.href = url
    }
  }
}
</script>
