---
date: "2018-05-25T12:00:00Z"
title: "Configure Replicated to Use Studio"
description: "Install Replicated and configure it to use Studio"
weight: "9012"
categories: [ "Replicated Studio Guide" ]
index: "guides/studio"
type: "chapter"
gradient: "redToRed"
icon: "replicatedCircle"
aliases: [/guides/configure-studio]
---

### Install Replicated with Studio configuration on the dev server

Use our simple installation script (on a Linux server in your IaaS provider of choice, or in a local dev environment in Vagrant/VirtualBox) to install Replicated. You'll be prompted for the ngrok hostname provided earlier during setup.

<h4 class="u-fontWeight--medium u-fontSize--large u-color--tuna u-marginBottom--more u-marginTop--more">Which scheduler are you using?</h4>
<div>
    <div class="flex">
        <h5 id="native-link" class="studioIntro--link">Native</h5>
        <h5 id="swarm-link" class="studioIntro--link">Docker</h5>
        <h5 id="kubernetes-link" class="studioIntro--link">Kubernetes</h5>
    </div>
</div>

<div class="studioIntro--installScript empty u-marginTop--more" style="display: block;">
    <p>Please select which scheduler you're running above.</p>
</div>

<div class="studioIntro--installScript native u-marginTop--more" style="display: none;">
    <pre class="language-bash">curl -sSL https://get.replicated.com/studio/native | sudo bash</pre>
</div>

<div class="studioIntro--installScript swarm u-marginTop--more" style="display: none;">
    <pre class="language-bash">curl -sSL https://get.replicated.com/studio/swarm  | sudo bash</pre>
</div>

<div class="studioIntro--installScript kubernetes u-marginTop--more" style="display: none;">
    <pre class="language-bash">curl -sSL https://get.replicated.com/studio/k8s | sudo bash</pre>
</div>

