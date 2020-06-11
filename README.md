<p># BrainMRI_Scan_FastAI_segmentation</p>
<p><strong>Objective</strong>: To use FASTAI unet learner to perform an image segmentation task i.e. to identify tumours from MRI of Brain. Also to log the loss metrices in Neptune AI logger and compare the results after hyperparameter tuning</p>
<p><strong>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;<img src="https://docs.fast.ai/imgs/u-net-architecture.png" alt="" width="303" height="202" /></strong></p>
<p><strong>Model Architecture:&nbsp;</strong></p>
<p id="We-will-be-using-the-DynamicUnet-architecture-for-the-following-from-fastai.vision">We will be using the DynamicUnet architecture for the following from fastai.visionThis U-Net will sit on top of an encoder (that can be a pretrained model) and with a final output of n_classes. During the initialization, it uses Hooks to determine the intermediate features sizes by passing a dummy input through the model and create the upward path automatically.</p>
<p>Pretrained model:&nbsp;resnet34&nbsp;</p>
<p id="Calling-the-unet_learner-and-using-pretrained-resnet34-architecture-as-its-initial-backbone-structure,metrics-used-is-dice-and-for-weight_decay(wd)-we-are-using-1e-1">metrics<strong>: </strong>DICE</p>
<p id="Calling-the-unet_learner-and-using-pretrained-resnet34-architecture-as-its-initial-backbone-structure,metrics-used-is-dice-and-for-weight_decay(wd)-we-are-using-1e-1">weight_decay(wd): 1e-1</p>
<p><strong>What is Neptune AI ?</strong></p>
<p>Experiment management tool bringing organization and collaboration to data science projects.link:&nbsp;<a href="https://neptune.ai/">https://neptune.ai/</a></p>
<p>&nbsp;</p>
<p><strong>Result:</strong></p>
<p><img src="https://www.kaggleusercontent.com/kf/30060909/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..gDlZm4yX1EpLE6DfA3f5pw.or7Dl0WxpHxT2c06B3wlw5z6e5iHgP5VnjSOzJWgbU35WC_MOEnrf86INSThf0yPPPwUFtyfIjgcVwTqIq_6psvC4Uzds6hFXWfAv9-YYcUBE_qoRbpQJCd7_ZS7u-k-SzP6WFTTI1KPdKWvuKNCriENmq_VZoToky5N8PMPzjyUmDOtL3V1ySI--InGGy31.Ruvn5dd7EiVmVIySmVGW6A/__results___files/__results___25_1.png" alt="" width="312" height="518" /></p>
<p><img src="https://www.kaggleusercontent.com/kf/30060909/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..2sms8jfAQKvqZNAf67mwsA.7l6I2I9j1i1ofmnLH0BNVdM_9tX60-yKGmMPvkHoptO7IzmRVLN4cpvQ4WtDM4rVUlBdbv1rPWUfvN13y0QsZ4ccl-izqLxhKb5jGUGoH6HE3aC_knlflEQOSL_QbIqMwnStsS9ovnbXOQeaFJLG_HQDNPNSsvDdeKeIJC1TW7SZjJn6rXMVN2OfCu34UAHyiBxWJ7MIHh6jeoKeJZjsL4WvqFxxrrIiko0uDOUgwrKRvpGhcS4wSDLDtaWbrEYoYMMG_kGJLg2SOa_0SUYkDiXk5jMp89g8Y6QrxctVG3ItLhg1FfsqMe6RvApe3Mrm-rh5fyKUIF_x6oUdHCcN_eGj1ghIy0jXVnc7FA-HnaxH5M6keRBba5sOMIN3ZycsRYnZpH7uNi4PtN1FXbgPT3g2_iy6EsM5aPcY6q3UfJtCqzNeDWV4IR6OWwsVbFbJJD_1lB9pRFI0mKHhoRDOJvZTbvXTBN3LpQ313xq3hrZjp-FpMiVy2823CCE5RXn6E1xTeOoY5N1YWj2QonKQ2mK_AWLXkYGVKEaU4YbgTNUf1uG6t98zBKSBl97t7VVJkDdZvpFKcwqEpDcWaNLUivNbN781WaZA10qpCM9SzF_e3Z1n83K-71H2xMEwNyDCccoFEOMx5YItZaEmU7Vnaz9KIpU38WsBr7R4zY4PH9xgZCJzapZahh-nJCiqHacYvkl_GHtNJpBD90Ve1O9Vpw.E9few75nZd9DwjJiY7iU6w/__results___files/__results___26_1.png" width="277" height="460" /></p>
<h4 id="This-U-Net-will-sit-on-top-of-an-encoder-(that-can-be-a-pretrained-model)-and-with-a-final-output-of-n_classes.-During-the-initialization,-it-uses-Hooks-to-determine-the-intermediate-features-sizes-by-passing-a-dummy-input-through-the-model-and-create-the-upward-path-automatically.">&nbsp;</h4>
<p># Publication :&nbsp;<a href="https://medium.com/p/71fbc56febba/edit">https://medium.com/p/71fbc56febba/edit</a></p>
<p># Dataset : https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation (by :Mateusz Buda)</p>
